idf_build_get_property(target IDF_TARGET)

if(${target} STREQUAL "esp32")
    idf_component_register(SRCS "esp_adc_cal_esp32.c"
                    INCLUDE_DIRS "include"
                    REQUIRES driver efuse)

elseif(${target} STREQUAL "esp32s2")
    idf_component_register(SRCS "esp_adc_cal_esp32s2.c"
                    INCLUDE_DIRS "include"
                    REQUIRES driver efuse)

elseif(${target} STREQUAL "esp32c3")
    idf_component_register(SRCS "esp_adc_cal_esp32c3.c"
                    INCLUDE_DIRS "include"
                    REQUIRES driver efuse)

elseif(${target} STREQUAL "esp32s3")
idf_component_register(SRCS "esp_adc_cal_esp32s3.c"
                INCLUDE_DIRS "include"
                REQUIRES driver efuse)


elseif(${target} STREQUAL "esp32h2")
    idf_component_register(SRCS "esp_adc_cal_esp32h2.c"
                    INCLUDE_DIRS "include"
                    REQUIRES driver efuse)
endif()
