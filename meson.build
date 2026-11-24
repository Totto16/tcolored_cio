project(
    'tcolored_cio',
    'c',
    license: 'MIT',
    meson_version: '>=1.3.0',
    default_options: {
        'buildtype': 'release',
        'optimization': '3',
        'c_std': ['gnu23', 'gnu11'],
        'warning_level': '3',
        'werror': 'true',
        'b_ndebug': 'if-release',
    },
    version: '1.0.0',
)

deps = []

deps += dependency(
    'tstr.h',
    allow_fallback: true,
    default_options: {
        'static_string_modification_behavior': 'error',
    },
    version: ['>=1.0.0', '<2'],
)

inc_dirs = []
src_files = []

subdir('src')


tcolored_cio_lib = library(
    'tcolored_cio_dep',
    src_files,
    include_directories: inc_dirs,
    install: true,
    version: meson.project_version(),
    dependencies: deps,
)

tcolored_cio_dep = declare_dependency(
    link_with: tcolored_cio_lib,
    include_directories: inc_dirs,
    version: meson.project_version(),
    dependencies: deps,
)

meson.override_dependency('tcolored_cio', tcolored_cio_dep)
