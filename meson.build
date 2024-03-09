project('libvct', 'c',
    meson_version: '>=1.2.0',
    version: '1.3.1'
)

fs = import('fs')

cc = meson.get_compiler('c')

libvct = fs.copyfile('prebuilt' / 'libvct.a')
nitrosdk_dep = dependency('NitroSDK')

libvct_dep = declare_dependency(
    dependencies: nitrosdk_dep,
    include_directories: include_directories('include'),
    link_with: libvct
)

meson.override_dependency('libvct', libvct_dep)
