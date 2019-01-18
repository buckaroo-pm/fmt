load('//:buckaroo_macros.bzl', 'buckaroo_deps_from_package')
load('//:subdir_glob.bzl', 'subdir_glob')

cxx_library(
  name = 'fmt',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('include', '**/*.h'),
  ]),
  srcs = glob([
    'src/**/*.cc',
  ]),
  platform_deps = [
    ('linux.*', buckaroo_deps_from_package('github.com/buckaroo-pm/host-pthread')),
  ],
  visibility = [
    'PUBLIC',
  ],
)
