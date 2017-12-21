# puzzCode (Puzzle Code)

![螢幕快照 2017-12-21 上午6.21.38.png](resources/02666CA47DBF6E48FF90A7D53556B865.png)

## Description

puzzCode is a simple compiler based on mingw, written in C# to build uncrackable windows application against analysis tools e.g. IDA, Ollydbg, x64dbg, etc.

puzzCode is based on MinGW to compile C/C++ source codes to assembly script. In addition, inserting some junk between every assembly instruction, turning orginal instruction into other obfuscated codes, and cuting each function into countless pieces! 

**The most important thing is ... exe file compiled by the same code will be different for Anti-Virus as a new born program!!**

Example: 
```
void play(void) {
    int code = rand() % 3;
    switch (code)
    {
      case 0:
        MessageBoxA(0, "hello", "info", 0);
        break;
      case 1:
        MessageBoxA(0, "hola", "info", 0);
        break;
      default:
        MessageBoxA(0, ":/ ...", "info", 0);
        break;
    }
}   
```

Normal Graph Overview (IDA)

It's pretty easy to understand, right?

![螢幕快照 2017-12-21 上午5.44.18.png](resources/F3D0B8CD285ECAD326C72873AA2D0146.png)

Graph Overview, Compiled via puzzCode (IDA)

... How about now :) ?

![螢幕快照 2017-12-21 上午6.16.17.png](resources/94BA0F1EF7491E9BE5F71BBE80881634.png)

---

## Quick Run

puzzCode only support 32bit Windows PE compiling currenly.

1. Install MinGW on your windows environment:
  https://sourceforge.net/projects/mingw/files/Installer

2. Download from [Release Page](https://github.com/aaaddress1/puzzCode/releases), Or clone this project, compile it with Visual C# 2017, you'll get puzzCode software.

## Usage

![螢幕快照 2017-12-21 上午5.36.29.png](resources/454D56B8EF05426D6AE99B82B2F8A166.png)

You have to set the MinGW path on your Windows environment for the first time running.
Besides,  compiler arguments, linker arguments, and obfuscated degree (from 0 to 100) are user adjustable.

![螢幕快照 2017-12-21 上午6.17.08.png](resources/89EFD46DE61B09F2793982E124C535B4.png)
![螢幕快照 2017-12-21 上午6.26.18.png](resources/D6DD734B6E8B5323148B0F707C5053B8.png)

After you setup the configurations, you are able to coding freely in puzzCode.
Simply hit the "Compile" button, the .exe file will be generated at the same path of your source code file.

### Snippet
![螢幕快照 2017-12-21 上午6.27.23.png](resources/7468CD0110210F9087DEB8A3FE84F929.png)

Some backdoors and programs are really useful, but you don't have that source code? That's Ok, your can use the `Snippet > RunPE` feature.

![螢幕快照 2017-12-21 上午6.29.06.png](resources/B123B443F08DF005A368FA6FD60B8EC9.png)

puzzCode packs the program you selected, and generate source code, **Just Compile, and Get New Born Backdoooooor!!**

*RunPE refer: https://github.com/Zer0Mem0ry/RunPE/blob/master/RunPE.cpp*

