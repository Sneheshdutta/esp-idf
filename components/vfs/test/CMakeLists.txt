set(srcdirs ".")
if(IDF_TARGET STREQUAL "esp32")
    list(APPEND srcdirs "esp32")
endif()

idf_component_register(SRC_DIRS ${srcdirs}
                       INCLUDE_DIRS .
                       REQUIRES unity test_utils vfs fatfs spiffs
                       LDFRAGMENTS linker.lf
                      )
