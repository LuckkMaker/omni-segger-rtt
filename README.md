# omni-segger-rtt

[![Version](https://img.shields.io/github/v/release/LuckkMaker/omni-segger-rtt)](https://github.com/LuckkMaker/omni-segger-rtt/releases/latest)


## Introduction

**omni-segger-rtt** 是 [omni-sdk](https://github.com/LuckkMaker/omni-sdk) 的一个组件库。它基于[SEGGER RTT](https://www.segger.com/products/debug-probes/j-link/technology/about-real-time-transfer)，增加 CMakeLists.txt 使其能够在 omni 项目中使用。

[omni-sdk](https://github.com/LuckkMaker/omni-sdk) 项目是一个利用 CMake 和 kconfig 构建的嵌入式开发框架，同时提供 HAL 层驱动和各种组件驱动。可以根据不同板卡、不同模块的需求，自由选择需要的组件，构建自己的固件。并且提供 dev container 的支持，可以在 docker 容器中快速开发、编译、调试固件，免去搭建开发环境的烦恼。

可以从 [releases page](https://github.com/LuckkMaker/omni-sdk/releases) 获取最新的 omni-sdk 版本。
