# nuttx board stm32f401-minimum

Kconfig add:

```
config ARCH_BOARD_STM32F401_MINIMUM
	bool "STM32F401CCU6 Minimum ARM Development Board"
	depends on ARCH_CHIP_STM32F401CC
	select ARCH_HAVE_LEDS
	select ARCH_HAVE_BUTTONS
	select ARCH_HAVE_IRQBUTTONS
	---help---
		A configuration for the STM32F401 Minimum board.
```
```
    default "stm32f401-minimum"         if ARCH_BOARD_STM32F401_MINIMUM
```
```
if ARCH_BOARD_STM32F401_MINIMUM
source "boards/arm/stm32/stm32f401-minimum/Kconfig"
endif
```
