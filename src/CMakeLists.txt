set(SOURCE_FILES "")
add_folder(Algorithms "*.c" "*.h" "*.cpp" "*.hpp")
add_folder(Kernel "*.c" "*.h" "*.cpp" "*.hpp")
add_folder(MeshFix "*.c" "*.h" "*.cpp" "*.hpp")
add_folder(TMesh "*.c" "*.h" "*.cpp" "*.hpp")

set(BUILD_TARGET "MeshFix")
add_executable(${BUILD_TARGET} ${SOURCE_FILES})

install(TARGETS ${BUILD_TARGET}
        EXPORT MeshFixTargets
        RUNTIME DESTINATION bin)