set (SOURCES
    arsenal.cpp
    deltafReader.cpp
    emissionfunction.cpp
    emissionfunction_polzn_kernels.cpp
    emissionfunction_resonance_decays.cpp
    emissionfunction_sampling_kernels.cpp
    emissionfunction_smooth_kernels.cpp
    gaussThermal.cpp
    iS3D.cpp
    ParameterReader.cpp
    readindata.cpp
    RuniS3D.cpp
    Table.cpp
    viscous_correction.cpp
    )

add_library(iS3D_lib SHARED ${SOURCES})
add_executable(iS3D ${SOURCES})


target_link_libraries (iS3D_lib gsl gslcblas)
target_link_libraries (iS3D gsl gslcblas)

install(TARGETS iS3D DESTINATION ${CMAKE_HOME_DIRECTORY})
