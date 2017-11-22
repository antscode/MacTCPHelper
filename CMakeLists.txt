cmake_minimum_required(VERSION 2.8)

# See: https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html
SET(CMAKE_CXX_FLAGS "-Ofast")

add_library(MacTCPHelper STATIC
	AddressXlation.h
	CvtAddr.c
	CvtAddr.h
	dnr.c
	TCPHi.c
	TCPHi.h
	TCPRoutines.c
	TCPRoutines.h
)

install(TARGETS MacTCPHelper
    DESTINATION "lib"
)

install(FILES AddressXlation.h CvtAddr.h TCPHi.h TCPRoutines.h
    DESTINATION "include/mactcp"
)