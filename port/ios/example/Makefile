#TARGET := iphone:clang
#TARGET_IPHONEOS_DEPLOYMENT_VERSION = 3.0
#ARCHS = armv7
ARCHS = arm64
TARGET = appletv
export GO_EASY_ON_ME=1
export SDKVERSION=10.2
THEOS_DEVICE_IP=apple-tv.local 

BTSTACK_ROOT=../../..
# VPATH += $(BTSTACK_ROOT)/platform/daemon/example

ADDITIONAL_CFLAGS  = -I.. \
	-I$(BTSTACK_ROOT)/src \
	-I$(BTSTACK_ROOT)/platform/daemon/src \
	-I$(BTSTACK_ROOT)/platform/posix  \
	-I$(BTSTACK_ROOT)/platform/corefoundation  \

ADDITIONAL_LDFLAGS = -L../src/.theos/obj -lBTstack

TOOL_NAME = inquiry l2cap_test rfcomm_echo rfcomm_cat rfcomm_test l2cap_server l2cap_throughput

inquiry_FILES          = $(BTSTACK_ROOT)/platform/daemon/example/inquiry.c
rfcomm_echo_FILES      = $(BTSTACK_ROOT)/platform/daemon/example/rfcomm_echo.c
rfcomm_cat_FILES       = $(BTSTACK_ROOT)/platform/daemon/example/rfcomm_cat.c
rfcomm_test_FILES      = $(BTSTACK_ROOT)/platform/daemon/example/rfcomm_test.c
l2cap_test_FILES       = $(BTSTACK_ROOT)/platform/daemon/example/test.c
l2cap_server_FILES     = $(BTSTACK_ROOT)/platform/daemon/example/l2cap_server.c
l2cap_throughput_FILES = $(BTSTACK_ROOT)/platform/daemon/example/l2cap_throughput.c

include $(THEOS)/makefiles/common.mk
include $(THEOS_MAKE_PATH)/tool.mk
include $(THEOS_MAKE_PATH)/aggregate.mk

SUBPROJECTS = WiiMoteOpenGLDemo
