data_extractor_sources = [
  'main.c',
  'data_extractor-window.c',
]

data_extractor_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

data_extractor_sources += gnome.compile_resources('data_extractor-resources',
  'data_extractor.gresource.xml',
  c_name: 'data_extractor'
)

executable('data-extractor', data_extractor_sources,
  dependencies: data_extractor_deps,
  install: true,
)
