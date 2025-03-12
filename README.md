# Zest_RTC_RV-8803-C7

Zest_RTC_RV-8803-C7 board support for Zephyr OS.

## Usage

This board enables the following component:

- [Micro Crystal AG RV-8803-C7](https://www.microcrystal.com/en/products/real-time-clock-rtc-modules/rv-8803-c7/) RTC

💡 This driver should also be added to your workspace:

- [Micro Crystal AG RV-8803 driver](https://github.com/catie-aq/zephyr_microcrystal-rv8803) for Zephyr OS

> [!NOTE]
> The node label for the RV-8803 component is `rv88030`. \
> The node label for the RV-8803 RTC api is `rv88030_rtc`. \
> The node label for the RV-8803 counter api is `rv88030_cnt`. \
> The node label for the RV-8803 clock api is `rv88030_clk`. \
> Shield name: `zest_rtc_rv-8803-c7`.
