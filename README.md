# MacTCPHelper
C helper functions for MacTCP on 68k classic Macs. The functions are sourced from old Apple sample code (see code comments) 
and modified to work with Retro68.

MacTCPHelper is designed to be built with the [Retro68 GCC cross-compiler](https://github.com/autc04/Retro68).

## Building & Installing
Execute these commands from the top level of the MacTCPHelper directory:

    cd ..
    mkdir MacTCPHelper-build
    cd MacTCPHelper-build
    cmake ../MacTCPHelper -DCMAKE_TOOLCHAIN_FILE=<<YOUR_PATH_TO_Retro68-build>>/toolchain/m68k-apple-macos/cmake/retro68.toolchain.cmake
    make install

This will compile the helper library and install the library and headers into the m68k-apple-macos toolchain.

## Using MacTCPHelper in your code
Once MacTCPHelper is installed in your toolchain, you can reference the header files like this:

    #include <mactcp/CvtAddr.h>
    #include <mactcp/TCPHi.h>

To link to the MacTCPHelper library using CMAKE:

    target_link_libraries(<<YOUR_TARGET>> MacTCPHelper)
