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
-IF:\Development\xHarbour.1.0.0\bcc740\BCC740\include\windows\crtl;F:\Development\xHarbour.1.0.0\bcc740\BCC740\include\windows\sdk;F:\Development\xHarbour.1.0.0\bcc740\BCC740\include\dinkumware
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

```.cfg
CC=BCC32
CFLAGS= -c -D__EXPORT__ -IF:\Development\xHarbour.1.0.0\xhb10264_bcc740\xharbour\include  -d -LF:\Development\xHarbour.1.0.0\xhb10264_bcc740\xharbour\lib
VERBOSE=YES
DELTMP=YES
```


### REFERENCIAS 
[xHarbour Binaries 1.2.3 Rev. 10264 for BCC 7.40](http://www.xharbour.org/index.asp?page=download/windows/binaries_win)<br>
[Embarcadero 32-bit BCC 7.40 Compiler (Evaluation Only!)](http://www.xharbour.org/index.asp?page=download/windows/required_win)<br>
[Harbour Reference Guide](https://harbour.github.io/doc/harbour.html#welcome-to-harbour)<br>