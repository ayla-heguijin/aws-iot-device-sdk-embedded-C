set( DEMO_NAME "mqtt_demo_plaintext" )
# Demo target.
add_executable(${DEMO_NAME})

target_sources(
    ${DEMO_NAME}
    PRIVATE
        "${DEMO_NAME}.c"
)

target_link_libraries(
    ${DEMO_NAME}
    PRIVATE
        mqtt   
)

target_include_directories(
    mqtt
    PUBLIC
        ${CMAKE_CURRENT_LIST_DIR}
)