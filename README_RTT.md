# Introduction #

This is a branch for lwip-head on RT-Thread RTOS. 


Simply for copy and delete upgrade method. This folder can't coexist with the current lwip folder, you should delete it.

If you want to use ipv6, you may define
#define RT_LWIP_IPV6
#define RT_LWIP_IPV6_AUTOCONFIG
#define RT_LWIP_CHECKSUM_BY_HARDWARE (recommended if supported)
in your rtconfig.h file

further more,
the lwip-head now support the icmp_hardware_checksum so you may have to modify your driver.

some chip will filter ipv6 packages, so you must enable the Receive_All function in those chip,
for example in STM32F2x7/F4x7
ETH_InitStructure.ETH_ReceiveAll = ETH_ReceiveAll_Enable;
is needed.
