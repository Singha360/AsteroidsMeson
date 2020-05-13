project('asteroids', 'cpp', default_options : ['cpp_std=c++17','buildtype=release','warning_level=0'], version: '0.0.1', license: 'unlicensed')
incdir = include_directories('../include')
thread = dependency('threads')

if build_machine.system() == 'linux'
    x11 = dependency('x11')
    gl = dependency('gl')
    png = dependency('libpng')
    deps = [x11, gl, png, thread]
    linkargs = ['-lstdc++fs']
else
    deps = [thread]
    linkargs = []
endif



executable(meson.project_name(), 'src/main.cpp', include_directories: incdir , dependencies: deps ,link_args : linkargs)


