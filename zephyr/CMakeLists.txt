if(${CONFIG_HAS_SEMTECH_LORAMAC})

set(ZEPHYR_CURRENT_LIBRARY loramac-node)

zephyr_library_include_directories(../src/boards)
zephyr_library_include_directories(../src/mac)
zephyr_library_include_directories(../src/radio)
zephyr_library_include_directories(../src/system)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacAdr.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMac.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacClassB.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacCommands.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacConfirmQueue.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacCrypto.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacParser.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/LoRaMacSerializer.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/peripherals/soft-se/aes.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/peripherals/soft-se/cmac.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/peripherals/soft-se/soft-se.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_SX1276 ../src/radio/sx1276/sx1276.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_SX126X ../src/radio/sx126x/sx126x.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_SX126X ../src/radio/sx126x/radio.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/system/timer.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/system/delay.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/system/systime.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/boards/mcu/utilities.c)

zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/region/Region.c)
zephyr_library_sources_ifdef(CONFIG_HAS_SEMTECH_LORAMAC ../src/mac/region/RegionCommon.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_EU868 ../src/mac/region/RegionEU868.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_US915 ../src/mac/region/RegionUS915.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_CN779 ../src/mac/region/RegionCN779.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_EU433 ../src/mac/region/RegionEU433.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_AU915 ../src/mac/region/RegionAU915.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_AS923 ../src/mac/region/RegionAS923.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_CN470 ../src/mac/region/RegionCN470.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_KR920 ../src/mac/region/RegionKR920.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_IN865 ../src/mac/region/RegionIN865.c)
zephyr_library_sources_ifdef(CONFIG_LORAMAC_REGION_RU864 ../src/mac/region/RegionRU864.c)

endif()
