set(appname iCubBielefeld02)

file(GLOB scripts ${CMAKE_CURRENT_SOURCE_DIR}/scripts/*.xml)
file(GLOB firmware ${CMAKE_CURRENT_SOURCE_DIR}/scripts/firmwareUpdate.txt)
file(GLOB conf ${CMAKE_CURRENT_SOURCE_DIR}/conf/*.ini)

yarp_install(FILES ${scripts} DESTINATION ${ICUBCONTRIB_ROBOTS_INSTALL_DIR}/${appname}/scripts)
yarp_install(FILES ${conf} DESTINATION ${ICUBCONTRIB_ROBOTS_INSTALL_DIR}/${appname})
yarp_install(DIRECTORY conf/camera DESTINATION ${ICUBCONTRIB_ROBOTS_INSTALL_DIR}/${appname}) 

