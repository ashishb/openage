add_sources(libopenage
	animation.cpp
	color.cpp
	geometry.cpp
	render_factory.cpp
	renderer.cpp
	shader_program.cpp
	tests.cpp
	text.cpp
	texture.cpp
	texture_array.cpp
	uniform_input.cpp
	util.cpp
	window.cpp
	window_event_handler.cpp
)

pxdgen(
	tests.h
)

add_subdirectory(camera/)
add_subdirectory(font/)
add_subdirectory(gui/)
add_subdirectory(resources/)
add_subdirectory(stages/)

if(OPENGL_FOUND)
    add_subdirectory(opengl/)
endif()

if(VULKAN_FOUND)
    add_subdirectory(vulkan/)
endif()
