project(webgallery)
set (webgallery_VERSION_MAJOR 0)
set (webgallery_VERSION_MINOR 1)

CMAKE_MINIMUM_REQUIRED(VERSION 2.4)
include(FindPerl)

CONFIGURE_FILE(
   ${CMAKE_CURRENT_SOURCE_DIR}/webgallery.in
   ${CMAKE_CURRENT_BINARY_DIR}/webgallery
   @ONLY
)

install (PROGRAMS
   ${CMAKE_CURRENT_BINARY_DIR}/webgallery
   DESTINATION bin
)

install (FILES
   index_bottom.html
   index_top.html
   picture.html
   thumbnail.html
   DESTINATION lib/webgallery
)
