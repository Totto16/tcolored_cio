src_files += files('fprintf.c', 'fprintf.h')

include_dir = get_option('prefix') / get_option('includedir')

install_headers(
    files('fprintf.h'),
    install_dir: include_dir / 'tcolored_cio',
    preserve_path: true,
)
