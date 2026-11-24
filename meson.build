project(
    'tcolored_cio',
    'c',
    license: 'MIT',
    meson_version: '>=1.3.0',
    default_options: {
        'buildtype': 'release',
        'optimization': '3',
        'c_std': ['c23', 'c11'],
        'warning_level': '3',
        'werror': 'true',
        'b_ndebug': 'if-release',
    },
    version: '1.0.0',
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
)

tcolored_cio_dep = declare_dependency(
    link_with: tcolored_cio_lib,
    include_directories: inc_dirs,
    version: meson.project_version(),
)

meson.override_dependency('tcolored_cio', tcolored_cio_dep)
