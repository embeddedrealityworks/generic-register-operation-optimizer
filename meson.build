project(
    'groov',
    'cpp',
    version : '0.1.0',
    license : 'MIT',
    meson_version : '>=1.1.0',
    default_options : [
        'cpp_std=c++23',
    ],
)

mp11_sub = subproject('mp11')
mp11_dep = mp11_sub.get_variable('mp11_dep')

async_sub = subproject('cpp-baremetal-senders-and-receivers')
async_dep = async_sub.get_variable('async_dep')

stdx_sub = subproject('cpp-std-extensions')
stdx_dep = stdx_sub.get_variable('stdx_dep')

groov_dep = declare_dependency(
    include_directories : include_directories('include'),
    dependencies : [mp11_dep, async_dep, stdx_dep],
)
