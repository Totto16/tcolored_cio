src_files += files('tcolored_cio.c', 'tcolored_cio.h')

inc_dirs += include_directories('.')

include_dir = get_option('prefix') / get_option('includedir')

install_headers(
    files('tcolored_cio.h'),
    install_dir: include_dir / 'tcolored_cio',
    preserve_path: true,
)

