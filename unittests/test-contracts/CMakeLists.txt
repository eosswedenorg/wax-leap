if( EOSIO_COMPILE_TEST_CONTRACTS )
   set(EOSIO_WASM_OLD_BEHAVIOR "Off")
   find_package( eosio.cdt REQUIRED )
endif()

if ("${CMAKE_GENERATOR}" STREQUAL "Ninja")
   add_compile_options(-fcolor-diagnostics)
endif()

add_subdirectory( asserter )
add_subdirectory( deferred_test )
add_subdirectory( get_sender_test )
add_subdirectory( get_table_test )
add_subdirectory( integration_test )
add_subdirectory( noop )
add_subdirectory( payloadless )
add_subdirectory( proxy )
add_subdirectory( ram_restrictions_test )
add_subdirectory( reject_all )
add_subdirectory( restrict_action_test )
add_subdirectory( snapshot_test )
add_subdirectory( test_api )
add_subdirectory( test_api_db )
add_subdirectory( test_api_multi_index )
add_subdirectory( test_ram_limit )
add_subdirectory( action_results )
add_subdirectory( wasm_config_bios )
add_subdirectory( params_test )
add_subdirectory( wax_rsa )
add_subdirectory( crypto_primitives_test )
add_subdirectory( get_block_num_test )
