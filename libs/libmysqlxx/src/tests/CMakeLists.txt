include_directories (${CMAKE_CURRENT_BINARY_DIR})

add_executable (mysqlxx_test mysqlxx_test.cpp)
add_executable (failover failover.cpp)

target_link_libraries (mysqlxx_test mysqlxx dbms ${RT_LIBRARIES})
target_link_libraries (failover mysqlxx ${Poco_Util_LIBRARY} ${Poco_Foundation_LIBRARY})
target_link_rt_by_force (failover)
