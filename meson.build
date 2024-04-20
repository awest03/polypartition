project('polypartition', 'cpp')

polypartition_src = []
subdir('src')

polypartition_include = include_directories('include')

polypartition = library(
    'polypartition',
    polypartition_src,
    include_directories: polypartition_include,
    install: true
)

polypartition_dep = declare_dependency(
    link_with: polypartition,
    include_directories: polypartition_include
)

polypartition_test_src = []
subdir('test')

executable(
    'polypartition-test',
    polypartition_test_src,
    dependencies: [ polypartition_dep ]
)