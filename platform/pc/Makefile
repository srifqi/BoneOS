BUILDROOT ?= ../..

NSRCS =


CSRCS = \
	drv/video/video.c \
	drv/pit/pit.c \
	drv/ps2/kbd/kbd.c \
	drv/driver.c \
	drv/ps2/kbd/scancodes.c \
	drv/ps2/kbd/kbd_layouts/scancodes_usa.c \
	drv/ps2/kbd/utils.c  \
	drv/pci/pci.c \
	cpu/interrupts/pic.c \
	drv/cmos/rtc/rtc.c \
	io/io.c \
	drv/pcspkr/pcspkr.c \
	drv/serial/serialport.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_LOW).c \
	drv/video/VGA/graphics/graphics.c \
	drv/video/VGA/graphics/vga_graphics.c
	
ifeq ($(VIDEO_DRIVER),VGA)
ifeq ($(VIDEO_DRIVER_MODE),textmode)
 CSRCS += \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/utils.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/putch.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/clear.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/term_scroll.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/vga_textmode.c \
	drv/video/$(VIDEO_DRIVER)/$(VIDEO_DRIVER_MODE)/update_cursor.c 
endif
endif



LIBNAME := platform

include $(BUILDROOT)/library.mk
