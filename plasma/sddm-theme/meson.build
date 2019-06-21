sddm_dir = join_paths(path_datadir, 'sddm', 'themes', 'SolusDark for breeze')
components_dir = join_paths(path_datadir, 'sddm', 'themes', 'SolusDark for breeze', 'components')
artwork_dir= join_paths(path_datadir, 'sddm', 'themes', 'SolusDark for breeze', 'components', 'artwork')

install_data(
    'Background.qml',
    'BreezeMenuStyle',
    'KeyboardButton.qml',
    'Login.qml',
    'Main.qml',
    'metadata.desktop',
    'preview.png',
    'SessionButton.qml',
    'theme.conf',
    install_dir: sddm_dir,
)

install_data(
    'ActionButton.qml',
    'Battery.qml',
    'Clock.qml',
    'KeyboardLayoutButton.qml',
    'SessionManagementScreen.qml',
    'UserDelegate.qml',
    'UserList.qml',
    'VirtualKeyboard.qml',
    'WallpaperFader.qml',
    install_dir: components_dir,
)


install_data(
    'logout:primary.svgz',
    'restart_primary.svgz',
    'shutdown_primary.svgz',
    'sddm_background.png',
    install_dir: artwork_dir,
)
