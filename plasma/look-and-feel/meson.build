solusdark_dir = join_paths(path_datadir, 'plasma', 'look-and-feel', 'solusdark.desktop')
contents_dir = join_paths(path_datadir, 'plasma', 'look-and-feel', 'solusdark.desktop', 'contents')
preview_dir = join_paths(path_datadir, 'plasma', 'look-and-feel', 'solusdark.desktop', 'contents', 'previews')
layouts_dir = join_paths(path_datadir, 'plasma', 'look-and-feel', 'solusdark.desktop', 'contents', 'layouts')

install_data(
    'metadata.desktop',
    'metadata.json',
    install_dir: solusdark_dir,
)

install_data(
    'defaults',
    install_dir: contents_dir,
)

install_data(
    'fullscreenpreview.jpg',
    'preview.png',
    install_dir: preview_dir,
)

install_data(
    'org.kde.plasma.desktop-layout.js',
    install_dir: layouts_dir,
)
