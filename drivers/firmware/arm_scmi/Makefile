# SPDX-License-Identifier: GPL-2.0-only
scmi-bus-y = bus.o
scmi-driver-y = driver.o notify.o
scmi-transport-$(CONFIG_ARM_SCMI_HAVE_SHMEM) = shmem.o
scmi-transport-$(CONFIG_ARM_SCMI_TRANSPORT_MAILBOX) += mailbox.o
scmi-transport-$(CONFIG_ARM_SCMI_TRANSPORT_SMC) += smc.o
scmi-transport-$(CONFIG_ARM_SCMI_HAVE_MSG) += msg.o
scmi-transport-$(CONFIG_ARM_SCMI_TRANSPORT_VIRTIO) += virtio.o
scmi-protocols-y = base.o clock.o perf.o power.o reset.o sensors.o system.o voltage.o
scmi-module-objs := $(scmi-bus-y) $(scmi-driver-y) $(scmi-protocols-y) \
		    $(scmi-transport-y)
obj-$(CONFIG_ARM_SCMI_PROTOCOL) += scmi-module.o
obj-$(CONFIG_ARM_SCMI_POWER_DOMAIN) += scmi_pm_domain.o
obj-$(CONFIG_QTI_SCMI_PMU_PROTOCOL) += pmu_vendor.o
obj-$(CONFIG_QTI_SCMI_C1DCVS_PROTOCOL) += c1dcvs_vendor.o
obj-$(CONFIG_QTI_SCMI_MEMLAT_PROTOCOL) += memlat_vendor.o
obj-$(CONFIG_QTI_SCMI_CPUFREQ_STATS_PROTOCOL) += cpufreq_stats_vendor.o
obj-$(CONFIG_QTI_SCMI_PLH_PROTOCOL) += plh_vendor.o
