# In case the platform does NOT support this type of sensors
ccflags-y += -I$(srctree)/drivers/misc/mediatek/hwmon/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/accelerometer/inc
ccflags-y += -I$(srctree)/drivers/misc/mediatek/magnetometer/inc
obj-y   +=  mag.o
obj-y   +=  mag_factory.o

ifeq ($(CONFIG_MTK_SCP_SENSORHUB_V1),y)
obj-$(CONFIG_MTK_MAGHUB)        +=  maghub/
else
obj-$(CONFIG_MTK_AKM09911_NEW)   +=  akm09911-new/
# [yanlin start] Porting sensors
obj-$(CONFIG_MTK_AKM09916_NEW)   +=  akm09916-new/
# [yanlin end]
endif
