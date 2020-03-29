find_package(SDL2 REQUIRED)
find_package(OpenSSL REQUIRED)

add_executable(std-browser src/main.cpp)
add_dependencies(std-browser css file html protocol)

target_include_directories(std-browser PRIVATE ${SDL2_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIR})
target_link_libraries(std-browser css file html protocol ${SDL2_LIBRARIES} ${OPENSSL_LIBRARIES})

install(
	TARGETS std-browser
	RUNTIME DESTINATION bin
)
