project('com.github.1enn0.transporter', 'vala', 'c')

gnome = import('gnome')
i18n = import('i18n')

add_global_arguments([
        '-DGETTEXT_PACKAGE="@0@"'.format(meson.project_name())
    ],
    language: 'c',
)

as_resources = gnome.compile_resources(
  'as-resources', 'data/' + meson.project_name() + '.gresource.xml',
  source_dir: 'data',
  c_name: 'as'
  )

executable(
    meson.project_name(),
    as_resources,
    'src/Transporter.vala',
    'src/TransporterWindow.vala',
    'src/Settings.vala',
    'src/Utils.vala',
    'src/WormholeInterface.vala',
    'src/View/AbstractView.vala',
    'src/View/ErrorView.vala',
    'src/View/InstallView.vala',
    'src/View/WelcomeView.vala',
    'src/View/ReceiveView.vala',
    'src/View/SendView.vala',
    'src/View/DropView.vala',
    'src/View/SettingsView.vala',
    dependencies: [
        dependency('gtk+-3.0'),
        dependency('granite'),
        dependency('glib-2.0', version: '>=2.30.0')
    ],
    install: true
)

subdir('data')
subdir('po')

meson.add_install_script('meson/post_install.py')
