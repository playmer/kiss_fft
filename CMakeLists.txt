Set(KissFFT_Source kiss_fft.c
                   _kiss_fft_guts.h
                   kiss_fft.h
                   kissfft.hh)

Get_Filename_Component(ParentDirectory ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)

Include_Directories(${ParentDirectory} ${CMAKE_CURRENT_SOURCE_DIR})

Add_Library(KissFFT ${KissFFT_Source})
Target_Compile_Definitions(KissFFT PUBLIC "_CRT_SECURE_NO_WARNINGS")
