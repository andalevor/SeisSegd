project('SeisSegd', 'c',
  version : '0.0.1',
  license : 'LGPL',
  default_options : ['c_std=c11'])
inc = include_directories('include', 'extern/mlib')
cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)
seistrace_dep = dependency('seistrace')
subdir('include')
subdir('src')
subdir('test')
pkg_mod = import('pkgconfig')
pkg_mod.generate(libraries : SeisSegd,
  version : '0.0.1',
  name : 'libseissegd',
  filebase : 'seissegd',
  description : 'A library for SEGD reading and writing.')
