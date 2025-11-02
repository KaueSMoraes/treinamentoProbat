//----------------------------------------------------------------------------//
// Very important: If you get a Memory OverBooked message when compiling,
// try to increase your DOS free Memory and also you may comment some
// of the following CH headers files that you don't use. As a example,
// try to remove:
//
// This problem does not appears if you use Clipper 5.2, so try to work
// with Clipper 5.2 which is really superb!
// 
//
//        * Dbf.ch     -->  Write  // Dbf.ch
//        * DDE.ch     -->    "    // DDE.ch
//        * DLL.ch     -->    "    // DLL.ch
//        * Objects.ch -->    "    // Objects.ch
//        * Video.ch   -->    "    // Video.ch
//
// Also, we propose you this config.sys which is _really_ excelent:
//
//  DEVICE=C:\DOS\HIMEM.SYS
//  DEVICE=C:\WINDOWS\EMM386.exe RAM 1024 FRAME=E000
//  REM /I=B000-B7FF     <<--- PLACE IT AT THE END OF THE ABOVE, ONLY FOR NON-WINDOWS USERS <g>
//  DEVICEHIGH=C:\DOS\RAMDRIVE.SYS /E 2024
//  DOS=HIGH,UMB
//  COUNTRY=034,,C:\DOS\COUNTRY.SYS
//  FILES=50
//  BUFFERS=25
//
//  And this autoexec.bat:
//
//  LH C:\DOS\SMARTDRV.EXE
//  @ECHO OFF
//  PROMPT $p$g
//  PATH C:\WINDOWS;C:\DOS;C:\CLIPPER5\BIN
//  SET CLIPPER=F50
//  LH KEYB SP,,C:\DOS\KEYBOARD.SYS
//  LH MOUSE
//
//----------------------------------------------------------------------------//
