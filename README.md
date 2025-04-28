# FPGA-SiI9134-HDMI-720P-Bars

## 项目概述
基于FPGA的SiI9134 HDMI发送芯片控制实验，实现720P@60Hz彩条显示。包含Verilog硬件配置代码、调试工具链和芯片技术文档。重点解决I²C地址配置歧义问题（手册地址需右移1位）。

## 功能特性
- ✅ FPGA生成720P时序：1280x720@60Hz
- ✅ SiI9134寄存器配置（修正I²C地址问题）
- ✅ RGB24动态彩条生成
- 📁 附完整开发资料：
  - SiI9134数据手册.pdf
  - 官方编程指南.pdf  
  - C语言参考例程（STM32版）

## 硬件要求
- FPGA开发板（已验证型号：Altera Cyclone IV EP4CE10）
- SiI9134 HDMI发送芯片
- HDMI显示器（支持720P@60Hz）
- 连接方式：
  - FPGA_I2C → SiI9134_SCL/SDA
  - FPGA_RGB24 → SiI9134视频总线

## 代码结构
/rtl
│
├── color_bar.v // 顶层模块（含以下子模块实例化）
│ ├── clk_hdmi // HDMI时钟生成（74.25MHz）
│ ├── vga_ctrl // 彩条生成与时序控制
│ └── sii9134_top // SiI9134配置引擎
│ └── sii9134_cfg.v // I²C配置模块（核心修正点）

# SiI9134_clor_bar
