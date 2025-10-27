# Summary of Changes in immortalwrt-mt798x

This report details the main changes in the `immortalwrt-mt798x` project compared to the upstream `ImmortalWrt` project.

## New Packages

The most significant change is the addition of the `package/mtk` directory, which contains a collection of packages that provide support for the MediaTek MT798x platform. These packages include:

*   **`mt_wifi`:** A closed-source Wi-Fi driver for the MediaTek MT798x SoCs.
*   **`warp`:** A hardware acceleration engine for the MediaTek platform.
*   **`wifi-profile`:** A configuration tool for the `mt_wifi` driver.
*   **`luci-app-mtk`:** A LuCI application for configuring the `mt_wifi` driver.
*   **`mtwifi-cfg`:** A new configuration tool for the `mt_wifi` driver.
*   **`luci-app-mtwifi-cfg`:** A LuCI application for the `mtwifi-cfg` tool.
*   **`luci-app-eqos-mtk`:** A LuCI application for configuring QoS on the MediaTek platform.
*   **`luci-app-turboacc-mtk`:** A LuCI application for configuring hardware acceleration.

## Kernel Modifications

The `immortalwrt-mt798x` project includes a large number of kernel patches that add support for the MediaTek MT798x SoCs. These patches are located in the `target/linux/mediatek/patches-5.4` directory and provide drivers for various hardware components, including:

*   Clocks
*   SPI
*   Networking
*   Crypto
*   I2C
*   PWM

## Configuration Changes

The build system has been configured to include the new MediaTek-specific packages and features. The `defconfig` files in the `defconfig` directory enable a large number of `CONFIG_MTK_*` and `CONFIG_PACKAGE_*mtk*` options, which ensures that the new drivers and applications are compiled and installed in the final firmware image.

## Base System Modifications

Several core ImmortalWrt components have been modified to support the MediaTek hardware and drivers. These changes include:

*   **`netifd`:** Patches have been applied to `netifd` to support the `mt_wifi` driver and its specific requirements.
*   **`iwinfo`:** The `iwinfo` tool has been patched to add support for the `mt798x` platform.

In summary, the `immortalwrt-mt798x` project is a fork of `ImmortalWrt` that has been heavily modified to support the MediaTek MT798x platform. The main changes include the addition of a closed-source Wi-Fi driver, a hardware acceleration engine, and a large number of kernel patches.
