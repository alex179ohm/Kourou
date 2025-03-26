project('kourou', 'rust', 
          version: '0.1',
    meson_version: '>= 1.0.0',
    license: 'GPL-3.0-or-later',
  default_options: [ 'warning_level=2', 'werror=false', ],
)

i18n = import('i18n')
gnome = import('gnome')


name = 'Kourou'
base_id = 'org.creavo.Kourou'
base_path = '/org/creavo/kourou'
vcs_tag = run_command('git', 'rev-parse', '--short', 'HEAD', check: false).stdout().strip()

subdir('data')
subdir('src')
subdir('po')

gnome.post_install(
     glib_compile_schemas: true,
    gtk_update_icon_cache: true,
  update_desktop_database: true,
)
