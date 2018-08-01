gnome = import('gnome')

transporter_sources = [
  'Settings.vala',
  'Transporter.vala',
  'TransporterWindow.vala',
  'Utils.vala',
  'View/AbstractView.vala',
  'View/DropView.vala',
  'View/ErrorView.vala',
  'View/InstallView.vala',
  'View/ReceiveView.vala',
  'View/SendView.vala',
  'View/SettingsView.vala',
  'View/WelcomeView.vala',
  'WormholeInterface.vala',
]

transporter_deps = [
  dependency('gtk+-3.0'),
  dependency('granite'),
  dependency('glib-2.0', version: '>=2.30.0')
]

transporter_sources += gnome.compile_resources(
  'transporter-resources',
  meson.project_name() + '.gresource.xml',
  c_name: 'transporter'
)

executable(
    meson.project_name(),
    transporter_sources,
    dependencies: [
      transporter_deps
    ],
    install: true
)
