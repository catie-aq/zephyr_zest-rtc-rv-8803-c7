# Zest_RTC_RV-8803-C7

Zest_RTC_RV-8803-C7 board support for Zephyr OS.

## Usage

This board enables the following component:

- [Micro Crystal AG RV-8803-C7](https://www.microcrystal.com/en/products/real-time-clock-rtc-modules/rv-8803-c7/) RTC.

💡 This driver should also be added to your workspace:

- [Micro Crystal AG RV-8803 driver](https://github.com/catie-aq/zephyr_microcrystal-rv8803).

:pushpin: This shield defines:

- an MFD device: `mfd_zest_rtc_rv8803_<port>`,
- an RTC device: `rtc_zest_rtc_rv8803_<port>`,
- a counter device: `counter_zest_rtc_rv8803_<port>`,
- a clock controller device: `clock_zest_rtc_rv8803_<port>`.

:triangular_ruler: To use this shield:

- Update your device tree by adding the `ZEST_RTC_RV8803_C7(port)` macro to the `app.overlay` file.\
  Replace `port` with the number of the Zest_Core port to which the shield is connected, e.g.:

  ```c
  ZEST_RTC_RV8803_C7(1) /* Zest_RTC_RV-8803-C7 connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_rtc_rv-8803-c7` to the west command.

## Advanced Usage

This shield can be hardware-modified to suit your application.

In that case, use instead the alternate variant of the shield:

- Update your device tree by adding the `ZEST_RTC_RV8803_C7_ALT(port, irq)` macro to the `app.overlay` file, with:
  - `port`: number of the Zest_Core port to which the shield is connected,
  - `irq`: MFD module IRQ pin (cf. [6tron connector](https://github.com/catie-aq/zephyr_6tron-connector/blob/main/dts/bindings/sixtron-bus.yaml)).

  ```c
  ZEST_RTC_RV8803_C7_ALT(1, DIO2) /* Zest_RTC_RV-8803-C7 connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_rtc_rv-8803-c7_alt` to the west command.
