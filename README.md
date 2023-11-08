# YY3568

![image](https://github.com/youyeetoo/YY3568/assets/150230106/b8d83bde-d7a9-4137-815f-edb75716341a)


<br>
<div style="background:#f8f9fa;">
  <p style="margin-left:1%; font-weight:bold;"> The YY3568 motherboard is based on Rockchip RK3568 chip platform, a quad-core 64-bit Cortex-A55 core with a main frequency of up to 2GHz, integrated dual-core architecture GPU and high-performance NPU, with excellent chip performance. The development board has many functional interfaces, powerful multimedia performance, and can play unique advantages in the fields of Internet of Things, industrial control, intelligent transportation and lightweight artificial intelligence.</p>
  <ol style="margin-left:1%; font-weight:bold;">
    <li>The board has 2 channels of DSI, 1 channel of HDMI and 1 channel of EDP display interface. Supports dual-screen different display output and 4K resolution. Powerful display performance, and adapted to self-developed 7-inch mipi screen and edp screen. It can bring strong advantages and lower costs in the fields of multi-screen advertising machines, electronic stop signs, self-service machines, industrial HMI and other fields.</li>
    <li>Built-in 2-way Gigabit Ethernet, which can access and transfer data from internal and external networks via dual network ports. With WIFI/BT, PCIE 3.0 interface and SIM socket, it can be connected to 4G communication module to improve network transmission efficiency. Meets the requirements of multi-network port products such as NVR and industrial gateways.</li>
    <li>The built-in 5-way serial port can greatly reduce the communication cost. 2-way IIC, can connect multiple IIC devices. 1-channel CAN, which can meet the needs of automotive electronics field.</li>
    <li>Onboard PCIE3.0 and SATA interface, support M.2 solid-state hard disk, SATA hard disk, high-capacity expandable hard disk.</li>
  </ol>
</div>
<br>


# Hardware Interface Definition
## Machine interface definition
![image](https://github.com/youyeetoo/YY3568/assets/150230106/203236d3-9c08-4555-a076-ed3f14c1b6f5)
![image](https://github.com/youyeetoo/YY3568/assets/150230106/e62169af-5dd9-4f40-8093-dc107cde48c3)

- [Specification *YY3568  development kit* *RK3568 module*](https://drive.google.com/drive/folders/10Swvzpfxq9yvEkk6DED6rVXyLRYziJap?usp=sharing)
- [YY3568 Development Board *Appearance* *Dimensions*  *Interface* *Schematic Diagram*](https://wiki.youyeetoo.com/en/YY3568/DevelopmentBoardIntroduction)
- [Quality inspection certificate *RoHS certificate* *CE certificate* *CE Test report* *FCC certificate* *FCC Test report* ](https://drive.google.com/drive/folders/147mRIOddlrTTtnrDvB14WZNLyrl9q0OS?usp=sharing )

## Interface reuse and conflict table
1. Power domain table
When using pins, refer to the power domain table. `Avoid burning pins due to excessive voltage`.

|  Die Power Domain   | PMUIO1 | PMUIO2  | VCCIO1 | VCCIO2 | VCCIO3 | VCCIO4 | VCCIO5 | VCCIO6 | VCCIO7 |
| :---  | :---  | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Supply Power Voltage1 | 3.3V | 3.3V | 3.3V |1.8V | 3.3V | 1.8V | 3.3V | 1.8V | 3.3V |

2. Interface multiplexing table
<table>
    <tbody>
    <tr>
        <th>module</th>
        <th>Pin</th>
        <th>sysfs path</th>
      	<th>Func1</th>
      	<th>Func2</th>
      	<th>Func3</th>
      	<th>Func4</th>
      	<th>Func5</th>
      	<th>Func6</th>
        <th>Die Power Domain</th>
    </tr>
    <tr>
        <td rowspan="2">UART2</td>
        <td>UART2_TX_M0_DEBUG</td>
        <td>/dev/ttyS2</td>
      	<td>GPIO0_D1_u</td>
      	<td>UART2_TX_M0</td>
      	<td></td><td></td><td></td><td></td>
      	<td>PMUIO2</td>
    </tr>
    <tr>
        <td>UART2_RX_M0_DEBUG</td>
        <td>/dev/ttyS2</td>
      	<td>GPIO0_D0_u</td><td>UART2_RX_M0</td><td></td><td></td><td> </td><td></td>
        <td>PMUIO2</td>
    </tr>
    <tr>
        <td rowspan="2">UART3</td>
        <td>UART3_TX_M1</td>
        <td>/dev/ttyS3</td>
      	<td>GPIO3_B7_d</td><td>LCDC_D22</td><td>PWM12_M0</td><td>GMAC1_TXEN_M0</td><td>UART3_TX_M1</td><td>PDM_SDI2_M2</td>
      	<td>VCCIO5</td>
    </tr>
    <tr>
        <td>UART3_RX_M1</td>
        <td>/dev/ttyS3</td>
      	<td>GPIO3_C0_d</td><td>LCDC_D23</td><td>PWM13_M0</td><td>GMAC1_MCLKINOUT
_M0</td><td>UART3_RX_M1</td><td>PDM_SDI3_M2</td>
        <td>VCCIO5</td>
    </tr>
    <tr>
        <td rowspan="2">UART4</td>
        <td>UART4_TX_M1</td>
        <td>/dev/ttyS4</td>
      	<td>GPIO3_B2_d</td><td>LCDC_D17</td><td>VOP_BT1120_D8</td><td>GMAC1_RXD1_M0</td><td>UART4_TX_M1 </td><td>PWM9_M0</td>
      	<td>VCCIO5</td>
    </tr>
    <tr>
        <td>UART4_RX_M1</td>
        <td>/dev/ttyS4</td>
      	<td>GPIO3_B1_d</td><td>LCDC_D16</td><td>VOP_BT1120_D7</td><td>GMAC1_RXD0_M0</td><td>UART4_RX_M1</td><td>PWM8_M0</td>
        <td>VCCIO5</td>
    </tr>
    <tr>
        <td rowspan="2">UART8</td>
        <td>UART8_TX_M0</td>
        <td>/dev/ttyS8</td>
      	<td>GPIO2_C5_d</td><td>I2S2_SDI_M0</td><td>GMAC0_RXER</td><td>UART8_TX_M0</td><td>SPI2_CS1_M0</td><td></td>
      	<td>VCCIO4</td>
    </tr>
    <tr>
        <td>UART8_RX_M0</td>
        <td>/dev/ttyS8</td>
      	<td>GPIO2_C6_d</td><td>CLK32K_OUT1</td><td>UART8_RX_M0</td><td>SPI1_CS1_M0</td><td></td><td></td>
        <td>VCCIO4</td>
    </tr>
    <tr>
        <td rowspan="2">UART9</td>
        <td>UART9_TX_M1</td>
        <td>/dev/ttyS9</td>
      	<td>GPIO4_C5_d</td><td>PWM12_M1</td><td>SPI3_MISO_M1</td><td>SATA1_ACT_LED</td><td>UART9_TX_M1 </td><td>I2S3_SDO_M1</td>
      	<td>VCCIO7</td>
    </tr>
    <tr>
        <td>UART9_RX_M1</td>
        <td>/dev/ttyS9</td>
      	<td>GPIO4_C6_d</td><td>PWM13_M1</td><td>SPI3_CS0_M1</td><td>SATA0_ACT_LED</td><td>UART9_RX_M1</td><td>I2S3_SDI_M1</td>
        <td>VCCIO7</td>
    </tr>
    <tr>
        <td rowspan="2">I2C1</td>
        <td>I2C1_SCL_TP</td>
        <td>/dev/i2c-1</td>
      	<td>GPIO0_B3_u</td><td>I2C1_SCL</td><td>CAN0_TX_M0</td><td>PCIE30X1_BUTTONRSTn</td><td>MCU_JTAG_TDO</td><td></td>
      	<td>PMUIO2</td>
    </tr>
    <tr>
        <td>I2C1_SDA_TP</td>
        <td>/dev/i2c-1</td>
      	<td>GPIO0_B4_u</td><td>I2C1_SDA</td><td>CAN0_RX_M0</td><td>PCIE20_BUTTONRSTn</td><td>MCU_JTAG_TCK</td><td></td>
        <td>PMUIO2</td>
    </tr>
    <tr>
        <td rowspan="2">I2C5</td>
        <td>I2C5_SCL_M0</td>
        <td>/dev/i2c-5</td>
      	<td>GPIO3_B3_d</td><td>LCDC_D18</td><td>VOP_BT1120_D9</td><td>GMAC1_RXDV_CRS_M0</td><td>I2C5_SCL_M0</td><td>PDM_SDI0_M2</td>
      	<td>VCCIO5</td>
    </tr>
    <tr>
        <td>I2C5_SDA_M0</td>
        <td>/dev/i2c-5</td>
      	<td>GPIO3_B4_d</td><td>LCDC_D19</td><td>VOP_BT1120_D10</td><td>GMAC1_RXER_M0</td><td>I2C5_SDA_M0</td><td>PDM_SDI1_M2</td>
        <td>VCCIO5</td>
    </tr>
    <tr>
        <td rowspan="2">CAN</td>
        <td>CAN1_TX_M1</td>
        <td>Network node can0</td>
      	<td>GPIO4_C3_d</td><td>PWM15_IR_M1</td><td>SPI3_MOSI_M1</td><td>CAN1_TX_M1</td><td>PCIE30X2_WAKEn_M2</td><td>I2S3_SCLK_M1</td>
      	<td>VCCIO7</td>
    </tr>
    <tr>
        <td>CAN1_RX_M1</td>
        <td>Network node can0</td>
      	<td>GPIO4_C2_d</td><td>PWM14_M1</td><td>SPI3_CLK_M1</td><td>CAN1_RX_M1</td><td>PCIE30X2_CLKREQn_M2</td><td>I2S3_MCLK_M1</td>
        <td>VCCIO7</td>
    </tr>  
    <tr>
      <td rowspan="4">TP</td>
      <td>GPIO0_A6</td>
      <td>/dev/input/event2</td>
      <td>GPIO0_A6_d</td><td>GPU_PWREN</td><td>SATA_CP_POD</td><td>PCIE30X2_CLKREQn_M0</td><td></td><td></td>
      <td>PMUIO1</td>
    </tr>
    <tr>
      <td>GPIO0_B7</td>
      <td>/dev/input/event2</td>
      <td>GPIO0_B7_d</td><td>PWM0_M0</td><td>CPUAVS</td><td></td><td></td><td></td>
      <td>PMUIO2</td>
    </tr>
    <tr>
      <td>I2C1_SCL_TP</td>
      <td>/dev/input/event2</td>
      <td>GPIO0_B3_u</td><td>I2C1_SCL</td><td>CAN0_TX_M0</td><td>PCIE30X1_BUTTONRSTn</td><td>MCU_JTAG_TDO</td><td></td>
      <td>PMUIO2</td>
    </tr>
    <tr>
      <td>I2C1_SDA_TP</td>
      <td>/dev/input/event2</td>
      <td>GPIO0_B4_u</td><td>I2C1_SDA</td><td>CAN0_RX_M0</td><td>PCIE20_BUTTONRSTn</td><td>MCU_JTAG_TCK</td><td></td>
      <td>PMUIO2</td>
    </tr>
    <tr>
      <td rowspan="24">30 Pin extension pin</td>
      <td>GSENSOR_INT_L_GPIO3_C1</td>
      <td>/sys/class/gpio/gpio113</td>
      <td>GPIO3_C1_d</td><td>LCDC_HSYNC</td><td>VOP_BT1120_D13</td><td>SPI1_MOSI_M1</td><td>PCIE20_PERSTn_M1</td><td>I2S1_SDO2_M2</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>SPDIF_TX_M1</td>
      <td>/proc/asound/cards</td>
      <td>GPIO3_C5_d</td><td>PWM15_IR_M0</td><td>SPDIF_TX_M1</td><td>GMAC1_MDIO_M0</td><td>UART7_RX_M1</td><td>I2S1_LRCK_RX_M2</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>GPIO3_A1</td>
      <td>/sys/class/gpio/gpio97</td>
      <td>GPIO3_A1_d</td><td>LCDC_D8</td><td>VOP_BT1120_D0</td><td>SPI1_CS0_M1</td><td>PCIE30X1_PERSTn_M1</td><td>SDMMC2_D0_M1</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>GPIO2_D7</td>
      <td>/sys/class/gpio/gpio95</td>
      <td>GPIO2_D7_d</td><td>LCDC_D7</td><td>VOP_BT656_D7_M0</td><td>SPI2_MISO_M1</td><td>UART8_TX_M1</td><td>I2S1_SDO0_M2</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>GPIO0_D4</td>
      <td>/sys/class/gpio/gpio28</td>
      <td>GPIO0_D4_d</td><td></td><td></td><td></td><td></td><td></td>
      <td>PMUIO0</td>
    </tr>
    <tr>
      <td>GPIO0_C0</td>
      <td>/sys/class/gpio/gpio16</td>
      <td>GPIO0_C0_d</td><td>PWM1_M0</td><td>GPUAVS</td><td>UART0_RX</td><td></td><td></td>
      <td>PMUIO2</td>
    </tr>
    <tr>
      <td>GPIO3_D4</td>
      <td>/sys/class/gpio/gpio124</td>
      <td>GPIO3_D4_d</td><td>CIF_D6</td><td>EBC_SDDO6</td><td>SDMMC2_DET_M0</td><td>I2S1_SDI2_M1</td><td>VOP_BT656_D6_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_CLK_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_D3_d</td><td>CIF_D5</td><td>EBC_SDDO5</td><td>SDMMC2_CLK_M0</td><td>I2S1_SDI1_M1</td><td>VOP_BT656_D5_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_D2_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_D0_d</td><td>CIF_D2</td><td>EBC_SDDO2</td><td>SDMMC2_D2_M0</td><td>I2S1_LRCK_TX_M1</td><td>VOP_BT656_D2_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_D3_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_D1_d</td><td>CIF_D3</td><td>EBC_SDDO3</td><td>SDMMC2_D3_M0</td><td>I2S1_SDO0_M1</td><td>VOP_BT656_D3_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_D0_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_C6_d</td><td>CIF_D0</td><td>EBC_SDDO0</td><td>SDMMC2_D0_M0</td><td>I2S1_MCLK_M1</td><td>VOP_BT656_D0_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_D1_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_C7_d</td><td>CIF_D1</td><td>EBC_SDDO1</td><td>SDMMC2_D1_M0</td><td>I2S1_SCLK_TX_M1</td><td>VOP_BT656_D1_M1</td>
      <td>VCCIO6</td>
    </tr>
    <tr>
      <td>SDMMC2_CMD_M0</td>
      <td>/dev/block/mmcblk1</td>
      <td>GPIO3_D2_d</td><td>CIF_D4</td><td>EBC_SDDO4</td><td>SDMMC2_CMD_M0</td><td>I2S1_SDI0_M1</td><td>VOP_BT656_D4_M1</td>
      <td>VCCIO6</td>
    </tr>
      <tr>
      <td>GPIO2_B1</td>
      <td>/sys/class/gpio/gpio73</td>
      <td>GPIO2_B1_d</td><td>SDMMC1_PWREN</td><td>I2C4_SDA_M1</td><td>UART8_RTSn_M0</td><td>CAN2_RX_M1</td><td></td>
      <td>VCCIO4</td>
    </tr>
    <tr>
      <td>GPIO0_D5</td>
      <td>/sys/class/gpio/gpio29</td>
      <td>GPIO0_D5_d</td><td></td><td></td><td></td><td></td><td></td>
      <td>PMUIO0</td>
    </tr>
    <tr>
      <td>GPIO3_A5</td>
      <td>/sys/class/gpio/gpio101</td>
      <td>GPIO3_A5_d</td><td>LCDC_D12</td><td>VOP_BT1120_D4</td><td>GMAC1_RXD3_M0</td><td>I2S3_SDO_M0</td><td>SDMMC2_CMD_M1</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>SARADC_VIN4</td>
      <td>/sys/bus/iio/devices/iio\:device0/in_voltage4_raw</td>
      <td>SARADC_VIN4</td><td></td><td></td><td></td><td></td><td></td>
      <td>PCIE30</td>
    </tr>
    <tr>
      <td>SARADC_VIN3</td>
      <td>/sys/bus/iio/devices/iio\:device0/in_voltage3_raw</td>
      <td>SARADC_VIN3</td><td></td><td></td><td></td><td></td><td></td>
      <td>PCIE30</td>
    </tr>
    <tr>
      <td>SARADC_VIN2</td>
      <td>/sys/bus/iio/devices/iio\:device0/in_voltage2_raw</td>
      <td>SARADC_VIN2</td><td></td><td></td><td></td><td></td><td></td>
      <td>PCIE30</td>
    </tr>
    <tr>
      <td>SARADC_VIN1</td>
      <td>/sys/bus/iio/devices/iio\:device0/in_voltage1_raw</td>
      <td>SARADC_VIN1</td><td></td><td></td><td></td><td></td><td></td>
      <td>PCIE30</td>
    </tr>
    <tr>
      <td>MULTI_PHY0_REFCLKN</td>
      <td>Reserved</td>
      <td>MULTI_PHY0_REFCLKN</td><td></td><td></td><td></td><td></td><td></td>
      <td>EDP</td>
    </tr>
      <tr>
      <td>MULTI_PHY0_REFCLKP</td>
      <td>Reserved</td>
      <td>MULTI_PHY0_REFCLKP</td><td></td><td></td><td></td><td></td><td></td>
      <td>EDP</td>
    </tr>
    <tr>
      <td>MULTI_PHY1_REFCLKP</td>
      <td>Reserved</td>
      <td>MULTI_PHY1_REFCLKP</td><td></td><td></td><td></td><td></td><td></td>
      <td>EDP</td>
    </tr>
    <tr>
      <td>MULTI_PHY1_REFCLKN</td>
      <td>Reserved</td>
      <td>MULTI_PHY1_REFCLKN</td><td></td><td></td><td></td><td></td><td></td>
      <td>EDP</td>
    </tr>
    <tr>
      <td rowspan="3">RTC</td>
      <td>I2C5_SCL_M0</td>
      <td>/sys/devices/platform/fe5e0000.i2c/i2c-5/5-0051/rtc/rtc0/time</td>
      <td>GPIO3_B3_d</td><td>LCDC_D18</td><td>VOP_BT1120_D9</td><td>GMAC1_RXDV_CRS_M0</td><td>I2C5_SCL_M0</td><td>PDM_SDI0_M2</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>I2C5_SDA_M0</td>
      <td>/sys/devices/platform/fe5e0000.i2c/i2c-5/5-0051/rtc/rtc0/time</td>
      <td>GPIO3_B4_d</td><td>LCDC_D19</td><td>VOP_BT1120_D10</td><td>GMAC1_RXER_M0</td><td>I2C5_SDA_M0</td><td>PDM_SDI1_M2</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>RTCIC_INT_L_GPIO0_D3</td>
      <td>/sys/devices/platform/fe5e0000.i2c/i2c-5/5-0051/rtc/rtc0/time</td>
      <td>GPIO0_D3_d</td><td></td><td></td><td></td><td></td><td></td>
      <td>PMUIO0</td>
    </tr>
    <tr>
      <td rowspan="2">LED</td>
      <td>GPIO3_A4</td>
      <td>/sys/class/leds/work/brightness</td>
      <td>GPIO3_A4_d</td><td>LCDC_D11</td><td>VOP_BT1120_D3</td><td>GMAC1_RXD2_M0</td><td>I2S3_LRCK_M0</td><td>SDMMC2_D3_M1</td>
      <td>VCCIO5</td>
    </tr>
    <tr>
      <td>GPIO2_B2</td>
      <td>/sys/class/leds/work1/brightness</td>
      <td>GPIO2_B2_u</td><td>SDMMC1_DET</td><td>I2C4_SCL_M1</td><td>UART8_CTSn_M0</td><td>CAN2_TX_M1</td><td></td>
      <td>VCCIO4</td>
    </tr>
    <tr>
      <td>IR</td>
      <td>PWM7_IR</td>
      <td>/dev/input/event0</td>
      <td>GPIO0_C6_d</td><td>PWM7_IR</td><td>SPI0_CS0_M0</td><td>PCIE30X2_PERSTn_M0</td><td></td><td></td>
      <td>PMUIO2</td>
    </tr>
    <tr>
      <td>FAN</td>
      <td>GPIO3_A6</td>
      <td>/sys/class/thermal/cooling_device0/cur_state</td>
      <td>GPIO3_A6_d</td><td>LCDC_D13</td><td>VOP_BT1120_CLK</td><td>GMAC1_TXCLK_M0</td><td>I2S3_SDI_M0</td><td>SDMMC2_CLK_M1</td>
      <td>VCCIO5</td>
    </tr>
    </tbody>
</table>

3. Conflict table

| 1 | The wifi interface and SATA interface of YY3568 use the same M.2. wifi and SATA cannot be used at the same time|
| :--- | :--- |
| 2 | On the software driver of YY3568, the vp0 and vp1 software interfaces can be adapted to HDMI, DSI0, DSI1 and EDP. You can choose two of these four display interfaces to adapt vp0 and vp1 |

