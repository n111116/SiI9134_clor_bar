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
  - C语言参考例程
