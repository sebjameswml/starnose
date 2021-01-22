set(MORPH_LIBS jsoncpp_lib ${HDF5_C_LIBRARIES} ${ARMADILLO_LIBRARY} ${ARMADILLO_LIBRARIES} ${OpenCV_LIBS} ${LAPACK_LIBRARIES} OpenGL::GL glfw Freetype::Freetype)

# BarrelEmerge model
add_executable(james_comp2 james1.cpp)
target_compile_definitions(james_comp2 PUBLIC FLT=float COMPILE_PLOTTING COMP2)
target_link_libraries(james_comp2 ${MORPH_LIBS})
