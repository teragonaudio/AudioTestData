cmake_minimum_required(VERSION 2.8)
project(AudioTestData)

set(installDir /usr/local/share/audiotestdata)
make_directory(${installDir})
add_custom_target(install
  COMMAND cp -r ${CMAKE_SOURCE_DIR}/audio ${installDir}
  COMMAND cp -r ${CMAKE_SOURCE_DIR}/midi ${installDir}
  COMMAND cp -r ${CMAKE_SOURCE_DIR}/plugins ${installDir}
  COMMAND cp -r ${CMAKE_SOURCE_DIR}/presets ${installDir}
)
