### Starting
[xHarbour](http://www.xharbour.org)<br>
[xHarbour Binaries 1.2.3 Rev. 10264 for BCC 7.40](http://www.xharbour.org/index.asp?page=download/windows/binaries_win)<br>
[Embarcadero 32-bit BCC 7.40 Compiler (Evaluation Only!)](http://www.xharbour.org/index.asp?page=download/windows/required_win)<br>
[Harbour Reference Guide](https://harbour.github.io/doc/harbour.html#welcome-to-harbour)
[Fivewin Brasil](http://fivewin.com.br/)<br>
[Ext. VsCode Harbour and xHarbour - Antonino Perricone](https://marketplace.visualstudio.com/items?itemName=aperricone.harbour)<br>

### Adicionando PATHs
```.env
F:\Development\xHarbour.1.0.0\xhb10264_bcc740\xharbour\bin
F:\Development\xHarbour.1.0.0\bcc740\BCC740\bin
```

### Editar arquivos de configuracões
> F:\Development\xHarbour.1.2.3\bcc740\BCC740\bin\bcc32.cfg
```.cfg
-6
-DHB_GUI
-DHB_INCLUDE_WINEXCHANDLER
-DHB_NO_PROFILER
-DHB_NO_TRACE
-DHB_WIN32_IO
-IF:\Development\xHarbour.1.2.3\bcc740\BCC740\include\windows\crtl;F:\Development\xHarbour.1.2.3\bcc740\BCC740\include\windows\sdk;F:\Development\xHarbour.1.2.3\bcc740\BCC740\include\dinkumware
-O
-O1
-O2
-OS
-Ob
-Oc
-Ov
-c
-d
-g0
-k-
-v-
-w
-w!
```
> F:\Development\xHarbour.1.2.3\bcc740\BCC740\bin\ilink32.cfg

```.cfg
-Gn
-LF:\Development\xHarbour.1.2.3\bcc740\BCC740\lib;F:\Development\xHarbour.1.2.3\bcc740\BCC740\lib\psdk
-aa
-x
```
> F:\Development\xHarbour.1.2.3\xhb10264_bcc740\xharbour\bin\harbour.cfg
```.cfg
CC=BCC32
CFLAGS= -c -D__EXPORT__ -IF:\Development\xHarbour.1.2.3\xhb10264_bcc740\xharbour\include  -d -LF:\Development\xHarbour.1.2.3\xhb10264_bcc740\xharbour\lib
VERBOSE=YES
DELTMP=YES
```
### Gerando Executavel / Build .exe
> xhbmk2 -hbexe main.prg
```bash
xhbmk2 -hbexe main.prg

xHarbour 1.2.3 Intl. (SimpLex) (Build 20201212)
Copyright 1999-2020, http://www.xharbour.org http://www.harbour-project.org/
Compiling 'main.prg'...
Generating C source output to 'C:\Users\Andre\AppData\Local\Temp\hbmk_d9d7dw.dir\main.c'...
Done.
Lines 5, Functions/Procedures 1, pCodes 9
C:\Users\Andre\AppData\Local\Temp\hbmk_d9d7dw.dir\main.c:
Turbo Incremental Link 6.90 Copyright (c) 1997-2017 Embarcadero Technologies, Inc.
```

### CLI xHarbour
```bash
Harbour Make (hbmk2) 3.2.0dev (r2020-04-20 13:01)
Copyright (c) 1999-present, Viktor Szakats
https://github.com/harbour/core/

Syntax:

  hbmk2 [options] [<script[s]>] <src[s][.prg|.c|.obj|.o|.rc|.res|.def|.po|.pot|.hbl|@.clp|.d|.ch]>

Options:

  -o<outname>         output file name
  -l<libname>         link with <libname> library. <libname> should be without
                      path, extension and 'lib' prefix (unless part of the
                      name). Do not add core Harbour libraries, they are
                      automatically added as needed. If <libname> starts with a
                      '-' character, the library will be removed from the list
                      of libraries at link time.
  -L<libpath>         additional path to search for libraries
  -i<p>|-incpath=<p>  additional path to search for headers
  -static|-shared     link with static/shared libs
  -gt<name>           link with GT<name> GT driver, can be repeated to link
                      with more GTs. First one will be the default at run-time
  -inc[-]             enable/disable incremental build mode (default: disabled)
  -hbexe              create executable (default)
  -hblib              create static library
  -hbdyn              create dynamic library (without linked Harbour VM)
  -hbdynvm            create dynamic library (with linked Harbour VM)
  -help               more help
```

### REFERENCIAS 
[xHarbour Binaries 1.2.3 Rev. 10264 for BCC 7.40](http://www.xharbour.org/index.asp?page=download/windows/binaries_win)<br>
[Embarcadero 32-bit BCC 7.40 Compiler (Evaluation Only!)](http://www.xharbour.org/index.asp?page=download/windows/required_win)<br>
[Harbour Reference Guide](https://harbour.github.io/doc/harbour.html#welcome-to-harbour)<br>