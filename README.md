# QT Linux下dump错误日志生成库

## 简介

本仓库提供了一个在QT Linux环境下使用的dump错误日志生成库。通过引入该库，您可以轻松地在应用程序中生成错误日志文件，便于调试和问题排查。

## 功能特点

- **简单易用**：只需在项目中声明类库位置，并在`main.cpp`中设置dump文件生成位置，即可快速集成。
- **自动生成日志**：当应用程序发生崩溃或异常时，自动生成dump文件，记录详细的错误信息。
- **跨平台支持**：虽然本库主要针对Linux环境，但也可以在其他平台上进行适配和使用。

## 使用方法

### 1. 引入类库

在您的QT项目中，打开`.pro`文件，并在其中声明类库的位置。例如：

```pro
# 在pro文件中声明类库位置
LIBS += -L/path/to/library -lmydump
```

### 2. 设置dump文件生成位置

在`main.cpp`文件中，声明dump文件的生成位置。例如：

```cpp
#include "QBreakpadInstance.h"

int main(int argc, char *argv[]) {
    QApplication app(argc, argv);

    // 设置dump文件生成位置
    QBreakpadInstance.setDumpPath("/path/to/crashes_fuao");

    // 其他代码...

    return app.exec();
}
```

### 3. 编译和运行

完成上述步骤后，编译并运行您的QT应用程序。当应用程序发生崩溃或异常时，系统会自动在指定位置生成dump文件，记录详细的错误信息。

## 注意事项

- 请确保在设置dump文件生成位置时，路径是有效的，并且应用程序对该路径有写权限。
- 如果需要在其他平台上使用该库，可能需要进行一些适配工作。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接
[QTLinux下dump错误日志生成库](https://pan.quark.cn/s/22e2631c11b2) 

(备用: [备用下载](https://pan.baidu.com/s/10y3kMWoreL_zNAebZgaJnA?pwd=oide))

## 说明

该仓库仅用于学习交流，请勿用于商业用途。
