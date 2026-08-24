# app-start-tools
用一个cpp文件模拟Linux上的Wine<br>
完全开源<br>

# 如何运行
## 从源代码编译
首先，克隆我们的仓库<br>
'''cmd
git clone https://github.com/HVGLER/app-start-tools.git && cd app-start-tools
'''<br>
随后，下载winlibs上的gcc，最好是支持c++11标准的，然后配置环境变量，然后重开一个cmd窗口，执行以下命令来编译程序<br>
'''cmd
g++ main.cpp -o main.exe -finput-charset=UTF-8 -fexec-charset=gbk -g3 -w -fno-ms-extensions -pipe -Werror=return-type -Werror=vla -lgdi32 -luser32 -lkernel32 -lcomctl32 -lpdh -D_DEBUG -lws2_32 -Wl,--stack,12582912 -lpdh
'''<br>
之后，就可以直接运行main.exe查看效果了！<br>

## 从预编译的main.exe
下载预编译的main.exe，最推荐，下载好了之后可以直接双击运行
