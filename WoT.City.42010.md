# IOT SENSOR NETWORK OVER WEB: Architecture description

* Copyright (C) 2016 WoT.City Inc.
* Authors: Jollen Chen

A standard system architecture desctiption. It aims to conform the ISO 42010 to guide system's design.

## 1. Introduction

本文討論一個 Healthcare 的物聯網系統架構，此架構可應用在 Healcare 有關的系統開發應用。本文目標是描述一份 best practice 與 methods，並提出一個 abstraction layers 設計。本架構亦包含一個家電控制的 subsystem。

本架構內容 components 都可以易於重用，同時也著試制定 component 的介面標準。

## 2. Basics of System Architectures

### 2.1 Sensor Networking

**Stakeholders**. 用戶（User）希望可以偵測居家空氣品質，並保障數據的私有性（Privacy）。架構師（Developer）希望能以 Web 開放標準建構系統，或滿足 W3C Web of Things 規範；考量未來產品線的擴充，須符合 ISO 42010 與 IEC 62304。

**Organization View**. 家裡（User）佈署sSensors，平台服務商（Platform）提供 Backend Service。專家（Experts）可得到觀看數據的授權，並提供 User 健康照護顧問。

**Viewpoints**. 使用 configuration script。使用 decomposition architecrure（eg. REST）。Software lifecycle 滿足 IEC 62304。

**Technical View**. Sensors 經由 IoT Gateway 推送（Push）數據給 Platform。使用 Web 開放標準。參照圖 2.1。

**Viewpoints**. 使用 SPA 設計 IoT App 與 IoT Cloud（Web Service Backend）。使用 FreeRTOS tasking 的 IoT Device。使用 RFC 7252。

![Figure 2-1](https://wotcity.com/images/block/coap-lwm2m.png)

#### 2.1.2 Hierarchy of the System
#### 2.1.3 System Components

### 2.2 Control Networking

描述控制的部份。
* 把系統 decomposite 成不同的 component 與 subsystem
* 降低整合的複雜度

**Stakeholder.** Lead developer 的考量（concerns）會將系統元件化，並採用 RTOS 做為 MCU 與應用程式的介面（Interface）。User 的考量，希望以 Mobile App 做為控制介面。

**Control View.** 如圖 2.1。

![control-device](https://cloud.githubusercontent.com/assets/1126021/12474758/818b1056-c058-11e5-92e0-3b79906a0439.png)

Fig 2-1: Abstraction Level and Hierarchy


**Communication Viewpoint.** 在沒有數據傳送的需求時，裝置與 App 間僅以 HTTP 協定交連（interoperate）即可。將 RTOS API 封裝為 GPIO 控制元件。

## 3. Development

## 4. Requirements in Viewpoints

## 5. Summary

## 6. Bibliography

## Acknowledge


