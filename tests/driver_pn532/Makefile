APPLICATION = driver_pn532
include ../Makefile.tests_common

FEATURES_REQUIRED = periph_i2c periph_gpio

USEMODULE += xtimer
USEMODULE += pn532

# set default device parameters in case they are undefined
TEST_PN532_I2C ?= I2C_DEV\(0\)
TEST_PN532_RESET ?= GPIO_PIN\(0,0\)
TEST_PN532_IRQ ?= GPIO_PIN\(0,1\)

# export parameters
CFLAGS += -DTEST_PN532_I2C=$(TEST_PN532_I2C)
CFLAGS += -DTEST_PN532_RESET=$(TEST_PN532_RESET)
CFLAGS += -DTEST_PN532_IRQ=$(TEST_PN532_IRQ)
CFLAGS += -DPN532_SUPPORT_I2C

CFLAGS += -I$(CURDIR)

include $(RIOTBASE)/Makefile.include
