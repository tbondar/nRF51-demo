TARGET_CHIP := NRF51822_QFAA_CA
BOARD := BOARD_PCA10001

CFLAGS += -DDEBUG_NRF_USER -DBLE_STACK_SUPPORT_REQD
ASMFLAGS += -D__HEAP_SIZE=0

C_SOURCE_FILES += main.c

# Services
C_SOURCE_FILES += ble_tps.c
C_SOURCE_FILES += ble_ias.c
C_SOURCE_FILES += ble_lls.c
C_SOURCE_FILES += ble_bas.c
C_SOURCE_FILES += ble_ias_c.c

# Libraries
C_SOURCE_FILES += ble_advdata.c
C_SOURCE_FILES += ble_srv_common.c
C_SOURCE_FILES += ble_conn_params.c
C_SOURCE_FILES += app_timer.c
C_SOURCE_FILES += softdevice_handler.c
C_SOURCE_FILES += ble_bondmngr.c
C_SOURCE_FILES += pstorage.c
C_SOURCE_FILES += crc16.c
C_SOURCE_FILES += app_button.c
C_SOURCE_FILES += app_gpiote.c
C_SOURCE_FILES += ble_error_log.c
C_SOURCE_FILES += ble_debug_assert_handler.c

# Includes
INCLUDEPATHS += -I"$(SDK_PATH)Include/s110"
INCLUDEPATHS += -I"$(SDK_PATH)Include/app_common"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble/ble_services"
INCLUDEPATHS += -I"$(SDK_PATH)Include/sd_common"

OUTPUT_FILENAME := ble_app_proximity
SDK_PATH = ../../../../tools/nrf51_sdk_v5.1.0/nrf51822/

# Uncomment correct line if you have s110 programmed on the chip.
DEVICE_VARIANT := xxaa
#DEVICE_VARIANT := xxab
USE_SOFTDEVICE := S110
#USE_SOFTDEVICE := S210

include $(SDK_PATH)Source/templates/gcc/Makefile.common
