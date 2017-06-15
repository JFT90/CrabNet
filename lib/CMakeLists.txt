FILE(GLOB ALL_CPP_SRCS ${RakNet_SOURCE_DIR}/Source/*.cpp)

IF(MSVC)
    add_definitions("/D WIN32 /D _CRT_NONSTDC_NO_DEPRECATE /D _CRT_SECURE_NO_DEPRECATE /GS- /GR-")
ENDIF(MSVC)

if( RAKNET_ENABLE_STATIC )
    add_subdirectory(LibStatic)
endif()

if( RAKNET_ENABLE_DLL )
    add_subdirectory(DLL)
endif()