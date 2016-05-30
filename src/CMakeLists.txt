
set(OpenDocumentThumbnail_SRCS opendocumentcreator.cpp)

qt5_add_resources(OpenDocumentThumbnail_SRCS opendocumentthumbnail.qrc)

add_library(opendocumentthumbnail MODULE ${OpenDocumentThumbnail_SRCS})

target_link_libraries(opendocumentthumbnail Qt5::Gui KF5::KIOWidgets KF5::Archive)

install(TARGETS opendocumentthumbnail DESTINATION ${PLUGIN_INSTALL_DIR} )

install(FILES  opendocumentthumbnail.desktop DESTINATION ${SERVICES_INSTALL_DIR})
