set (tests
tMVAngle
tMVPosition
tMVTime
tQuantum
tQuantumHolder
tQVector
tUnit
)

foreach (test ${tests})
    add_executable (${test} ${test}.cc)
    target_link_libraries (${test} casa_casa)
    add_test (${test} ${CMAKE_SOURCE_DIR}/cmake/cmake_assay ./${test})
endforeach (test)
