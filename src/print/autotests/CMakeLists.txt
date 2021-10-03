set( EXECUTABLE_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR} )

include_directories( ${CMAKE_CURRENT_SOURCE_DIR}/.. ${CMAKE_CURRENT_SOURCE_DIR}/../.. )

set( knotes_knotesgrantleeprint_source knotesgrantleeprinttest.cpp  )
add_executable( knotesgrantleeprinttest ${knotes_knotesgrantleeprint_source})
add_test(NAME knotesgrantleeprinttest COMMAND knotesgrantleeprinttest)
ecm_mark_as_test(knotesgrantleeprinttest)
target_link_libraries( knotesgrantleeprinttest
    knotesprivate
    KF5::AkonadiNotes
    KF5::AkonadiCore
    KF5::GrantleeTheme
    KF5::Grantlee
    KF5::Mime
    Qt::Test
    Qt::Gui
)

