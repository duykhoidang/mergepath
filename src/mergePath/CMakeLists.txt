set(MERGE_PATH_SRC_FILES
    mergePath.cu mergePath.cuh
)

add_library(
    mergePath STATIC
    ${MERGE_PATH_SRC_FILES}
)

set_property(TARGET mergePath PROPERTY CUDA_ARCHITECTURES "75;86")
set_property(TARGET mergePath PROPERTY CUDA_STANDARD 17)

target_link_libraries(
    mergePath PRIVATE
    "cudart_static"
    "cuda"
)
