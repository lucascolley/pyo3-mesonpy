# meson.build
project('pyo3-mesonpy', 'rust', meson_version: '>=1.11.0')
py = import('python').find_installation(pure: false)
rustmod = import('rust')

cargo_ws = rustmod.workspace()
pkg = cargo_ws.package()

py.extension_module(
  'pyo3_mesonpy',
  'src/lib.rs',
  rust_dependency_map : pkg.rust_dependency_map(),
  rust_args: pkg.rust_args(),
  dependencies : pkg.dependencies(),
  install: true,
)
