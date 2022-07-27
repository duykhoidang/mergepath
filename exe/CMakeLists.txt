add_executable(main main.cu)

set_property(TARGET main PROPERTY CUDA_ARCHITECTURES "75;86")
set_property(TARGET main PROPERTY CUDA_STANDARD 17)

target_include_directories(
    main PRIVATE
    "${CMAKE_SOURCE_DIR}/src/mergePath"
)
target_link_libraries(
    main PRIVATE
    mergePath
)