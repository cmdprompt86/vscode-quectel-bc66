# VSCode Quectel BC66 Builder 
* version 1.0.1

## Install

Move folder **VSC_BC66** to VSCode - Projects - Workspace folder

Open folder **VSC_BC66** and paste Quectel SDK folder
    example: **BC66_OpenCPU_NB1_SDK_V1.4**

VSCode - Workspace - Add folder **VSC_BC66** to workspace

* Open .vscode/tasks.json and edit **BC66_OpenCPU_NB1_SDK_V1.4** and COM port
* Open .vscode/c_cpp_properties.json and edit **BC66_OpenCPU_NB1_SDK_V1.4**
* * used only for [IntelliSense](https://code.visualstudio.com/docs/editor/intellisense)
* * C/C++ Extension must exist

In **BC66_OpenCPU_NB1_SDK_V1.4** folder create your Project folder

Open VSC_BC66/Makefile and re-edit your settings

Click CTRL + SHIF + B to build or upload application

![Project](https://raw.githubusercontent.com/Wiz-IO/vscode-quectel-bc66/master/shot.png) 


## Other platforms and compilers ( edit Makefile paths to compiler )
* DARWIN
* * [GCC](https://dl.bintray.com/platformio/dl-packages/toolchain-gccarmnoneeabi-darwin_x86_64-1.70201.0.tar.gz)
* LINUX
* * [GCC](https://dl.bintray.com/platformio/dl-packages/toolchain-gccarmnoneeabi-linux_x86_64-1.70201.0.tar.gz)
* WINDOWS
* * [GCC](https://dl.bintray.com/platformio/dl-packages/toolchain-gccarmnoneeabi-windows-1.70201.0.tar.gz)

```
GCC_PATH        = C:/gccarmnoneeabi
ENV_PATH        = $(GCC_PATH)/bin
ENV_INC         = $(GCC_PATH)/arm-none-eabi/include
ENV_LIB_EABI    = $(GCC_PATH)/arm-none-eabi/lib/hard
ENV_LIB_GCC     = $(GCC_PATH)/arm-none-eabi/lib/hard
ENV_LIB         = -L$(ENV_LIB_EABI) -L$(ENV_LIB_GCC)
CC              = $(ENV_PATH)/arm-none-eabi-gcc
OC              = $(ENV_PATH)/arm-none-eabi-objcopy
```

>If you want to help / support:   
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ESUP9LCZMZTD6)

