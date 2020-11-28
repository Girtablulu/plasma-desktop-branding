project(
    'plasma-desktop-branding',
    ['c'],
    version: '3.1',
    license: [
        'Apache-2.0',
    ],
    default_options: [
        'prefix=/usr',
        'sysconfdir=/etc',
    ],
)

path_prefix = get_option('prefix')
path_datadir = join_paths(path_prefix, get_option('datadir'))

# Solusism

path_envdir = get_option('with-env-dir')
if path_envdir == ''
    path_envdir = join_paths(path_datadir, 'xdg', 'plasma-workspace', 'env')
endif

# Solus install paths

path_desktoptheme = join_paths(path_datadir, 'plasma', 'desktoptheme', 'solus-dark')
path_lookandfeel = join_paths(path_datadir,  'plasma', 'look-and-feel')
path_wallpapers = join_paths(path_datadir, 'wallpapers', 'SolusPlasma')
path_sddm = join_paths(path_datadir, 'sddm', 'sddm.conf.d')

wallpapers_files = [ 
    '1366x768.jpg',
    '1920x1080.jpg',
    '2560x1440.jpg',
    '3200x1800.jpg',
    '3840x2160.jpg',
    '5120x2880.jpg'
]

xdg_files = [
    'baloofilerc',
    'breezerc',
    'dolphinrc',
    'katepartrc',
    'kcm-about-distrorc',
    'kcminputrc',
    'kded5rc',
    'kdeglobals',
    'klaunchrc',
    'klipperrc',
    'konversationrc',
    'kscreenlockerrc',
    'ksmserverrc',
    'ksplashrc',
    'kwinrc',
    'kwinrulesrc',
    'plasmarc',
    'spectaclerc',
]

# Install files

install_data(['applications/kde-mimeapps.list'],
    install_dir : join_paths(path_datadir)
)

install_data(['env/50-solus-defaults.sh'],
    install_dir : path_envdir
)

# Plasma color-schemes

install_data(['plasma/color-schemes/SolusDark.colors'],
    install_dir : join_paths(path_datadir, 'color-schemes')
)

# Plasma desktoptheme

install_data(['plasma/desktoptheme/colors', 'plasma/desktoptheme/metadata.desktop'],
    install_dir : path_desktoptheme
)

# Plasma look-and-feel

install_data(['plasma/look-and-feel/metadata.desktop', 'plasma/look-and-feel/metadata.json'],
    install_dir : path_lookandfeel
)

install_data(['plasma/look-and-feel/defaults'],
    install_dir : join_paths(path_lookandfeel, 'contents')
)

install_data(['plasma/look-and-feel/fullscreenpreview.jpg', 'plasma/look-and-feel/preview.png'],
    install_dir : join_paths(path_lookandfeel, 'contents', 'previews')
)

# Plasma wallpapers

install_data(['plasma/wallpapers/metadata.desktop'],
    install_dir : path_wallpapers
)

install_data(['plasma/wallpapers/screenshot.jpg'],
    install_dir : join_paths(path_wallpapers, 'contents')
)

foreach i : wallpapers_files
    install_data(['plasma/wallpapers/' +i],
    install_dir : join_paths(path_wallpapers, 'contents', 'images')
    )
endforeach

# sddm

install_data(['sddm/20_plasma_config.conf', 'sddm/99_plasma_livecd.conf'],
    install_dir : path_sddm
)

# xdg

foreach i : xdg_files
    install_data(['xdg/' +i],
    install_dir : join_paths(path_datadir, 'xdg')
    )
endforeach

# Build Message

report = [
    '    Build configuration:',
    '    ====================',
    '',
    '    prefix:                                 @0@'.format(path_prefix),
    '    datadir:                                @0@'.format(path_datadir),
    '    envdir:                                 @0@'.format(path_envdir),
]

# Output some stuff to validate the build config
message('\n\n\n' + '\n'.join(report) + '\n\n')
