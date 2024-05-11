file(GLOB SIGN_SRC LIST_DIRECTORIES true "${CMAKE_CURRENT_SOURCE_DIR}/*")
set(DIRS "")


foreach(subdir ${SIGN_SRC})
    if(IS_DIRECTORY ${subdir})
        string(REGEX REPLACE ".*/([^/]*)$" "\\1" LAST_DIR ${subdir})
        message(STATUS "dir name is :${LAST_DIR}")
        list(APPEND DIRS ${LAST_DIR})
    endif()
endforeach()

list(REMOVE_ITEM DIRS "image")
foreach(item ${DIRS})
    message(STATUS "generate dir ${item} ...")
    ADD_SUBDIRECTORY(${item})
endforeach()