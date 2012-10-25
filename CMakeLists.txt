cmake_minimum_required(VERSION 2.8)
project(AudioTestData)

set(installDir /usr/local/share/audiotestdata)
add_custom_target(install
  COMMAND ${CMAKE_COMMAND} -E
    make_directory ${installDir}
  COMMAND ${CMAKE_COMMAND} -E
    copy_directory ${CMAKE_SOURCE_DIR}/audio ${installDir}/audio
  COMMAND ${CMAKE_COMMAND} -E
    copy_directory ${CMAKE_SOURCE_DIR}/midi ${installDir}/midi
  COMMAND ${CMAKE_COMMAND} -E
    copy_directory ${CMAKE_SOURCE_DIR}/plugins ${installDir}/plugins
  COMMAND ${CMAKE_COMMAND} -E
    copy_directory ${CMAKE_SOURCE_DIR}/presets ${installDir}/presets
)
