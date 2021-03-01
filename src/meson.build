gtk_test_vala_sources = [
  'main.vala',
  'window.vala',
]

gtk_test_vala_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

gtk_test_vala_sources += gnome.compile_resources('gtk_test_vala-resources',
  'gtk_test_vala.gresource.xml',
  c_name: 'gtk_test_vala'
)

executable('gtk_test_vala', gtk_test_vala_sources,
  vala_args: '--target-glib=2.50',  dependencies: gtk_test_vala_deps,
  install: true,
)
