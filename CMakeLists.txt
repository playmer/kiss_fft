Set(KissFFT_Source kiss_fft.c
                   _kiss_fft_guts.h
                   kiss_fft.h
                   kissfft.hh)

Get_Filename_Component(ParentDirectory ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)

Add_Library(KissFFT ${KissFFT_Source})
Target_Compile_Definitions(KissFFT PRIVATE _CRT_SECURE_NO_WARNINGS)

Target_Include_Directories(KissFFT PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
