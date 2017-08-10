include_directories("../include")
include_directories("common")

file(GLOB common_sources "common/*.h" "common/*.cc")

include_directories(SYSTEM "${PROJECT_BINARY_DIR}/generated")
include_directories(SYSTEM "${CMAKE_SOURCE_DIR}/contrib/SDL-mirror/include")

#bot_simple
add_executable(own_bot "own_bot.cc")
set_target_properties(own_bot PROPERTIES FOLDER examples)
target_link_libraries(own_bot sc2api sc2lib sc2utils)

