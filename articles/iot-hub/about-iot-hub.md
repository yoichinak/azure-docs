---
title: What is Azure IoT Hub | Microsoft Docs
description: This article explains the uses for an Azure IoT Hub. It allows you to read data in a scalable manner, and enables you to manage devices securely.
author: robinsh
ms.author: robinsh
ms.date: 05/03/2021
ms.topic: overview
ms.custom:  [mvc, amqp, mqtt, 'role: Direction', 'role: System Architecture', 'contentperf:fy21q3']
ms.service: iot-hub
services: iot-hub
---

# What is Azure IoT Hub

IoT Hub is a managed service hosted in the cloud that acts as a central message hub for communications in both directions between an IoT application and its attached devices. You can connect millions of devices and their backend solutions reliably and securely. Almost any device can be connected to an IoT Hub. 

Several messaging patterns are supported, including device-to-cloud telemetry, uploading files from devices, and request-reply methods to control your devices from the cloud. IoT Hub also supports monitoring to help you track creating devices, connecting devices, and device failures.

With IoT Hub's capabilities, you can build scalable, full-featured IoT solutions such as managing industrial equipment used in manufacturing, tracking valuable assets in healthcare, and monitoring office building usage.

## Scale your solution

IoT Hub scales to millions of simultaneously connected devices and millions of events per second to support your IoT workloads. For more information about scaling your IoT Hub, see [IoT Hub Scaling](iot-hub-scaling.md). To learn more about the multiple tiers of service offered by IoT Hub and how to best fit your scalability needs, check out the [pricing page](https://azure.microsoft.com/pricing/details/iot-hub/).

## Secure your communications

You can send data securely using IoT Hub.

* Per-device authentication enables each device to connect securely to IoT Hub and for each device to be managed securely.

* You have complete control over device access and can control connections at the per-device level.

* The [IoT Hub Device Provisioning Service](../iot-dps/index.yml) automatically provisions devices to the right IoT hub when the device first boots up.

* Multiple authentication types enable support of a variety of device capabilities:

  * SAS token-based authentication allows you to quickly get started with your IoT solution.

  * Individual X.509 certificate authentication is available for secure, standards-based authentication.

  * X.509 CA authentication can be used for simple, standards-based enrollment.

## Route device data

Built-in message routing functionality gives you flexibility to set up automatic rules-based message fan-out:

* [Message routing](iot-hub-devguide-messages-d2c.md) is used to control where your hub sends device telemetry.

* There is no additional cost to route messages to multiple endpoints.

* Routing rules can be configured to automatically direct messages based on content in those messages without having to write any code.

## Integrate with other services

You can integrate IoT Hub with other Azure services to build complete, end-to-end solutions. For example, use:

* [Azure Event Grid](../event-grid/index.yml) to enable your business to react quickly to critical events in a reliable, scalable, and secure manner.

* [Azure Logic Apps](../logic-apps/index.yml) to automate business processes.

* [Azure Machine Learning](iot-hub-weather-forecast-machine-learning.md) to add machine learning and AI models to your solution.

* [Azure Stream Analytics](../stream-analytics/index.yml) to run real-time analytic computations on the data streaming from your devices.

## Configure and control your devices

You can manage your devices connected to IoT Hub with an array of built-in functionality.

* Store, synchronize, and query device metadata and state information for all your devices.

* Set device state either per-device or based on common characteristics of devices.

* Automatically respond to a device-reported state change with message routing integration.

## Make your solution highly available

IoT Hub has a 99.9% [Service Level Agreement for IoT Hub](https://azure.microsoft.com/support/legal/sla/iot-hub/). The full [Azure SLA](https://azure.microsoft.com/support/legal/sla/) explains the guaranteed availability of Azure as a whole.

## Connect your devices

Use the [Azure IoT device SDK](./iot-hub-devguide-sdks.md) libraries to build applications that run on your devices and interact with IoT Hub. Supported platforms include multiple Linux distributions, Windows, and real-time operating systems. Supported languages include:

* C
* Embedded C
* C#
* Java
* Python
* Node.js.

IoT Hub and the device SDKs support the following protocols for connecting devices:

* HTTPS
* AMQP
* AMQP over WebSockets
* MQTT
* MQTT over WebSockets

IoT Hub and the device SDKs support the [Azure IoT Plug and Play](../iot-pnp/overview-iot-plug-and-play.md) conventions for connecting devices. IoT Plug and Play devices use a device model to advertise their capabilities to IoT Plug and Play-enabled applications. The device model enables solution builders to integrate smart devices with their solutions without any manual configuration.

If your solution cannot use the device libraries, devices can use the MQTT v3.1.1, HTTPS 1.1, or AMQP 1.0 protocols to connect natively to your hub.

If your solution cannot use one of the supported protocols, you can extend IoT Hub to support custom protocols:

* Use [Azure IoT Edge](../iot-edge/index.yml) to create a field gateway to perform protocol translation on the edge.

* Customize the [Azure IoT protocol gateway](https://github.com/Azure/azure-iot-protocol-gateway/blob/master/README.md) to perform protocol translation in the cloud.

## Quotas and limits

Each Azure subscription has default quota limits in place to prevent service abuse. These limits could impact the scope of your IoT solution. The current limit on a per-subscription basis is 50 IoT hubs per subscription. You can request quota increases by contacting support. For more information, see [IoT Hub Quotas and Throttling](iot-hub-devguide-quotas-throttling.md). For more details on quota limits, see one of the following articles:

* [Azure subscription service limits](../azure-resource-manager/management/azure-subscription-service-limits.md)

* [IoT Hub throttling and you](https://azure.microsoft.com/blog/iot-hub-throttling-and-you/)

## IoT Hub on Azure Stack Hub (preview)

IoT Hub on Azure Stack Hub (preview) allows you to create hybrid IoT solutions. IoT Hub is a managed service, acting as a central message hub for bi-directional communication between your IoT application and the devices it manages. You can use IoT Hub on Azure Stack Hub to build IoT solutions with reliable and secure communications between IoT devices and your on-premises solutions.

IoT Hub on Azure Stack Hub is free during public preview. For more information, see the [IoT Hub on Azure Stack Hub overview](/azure-stack/operator/iot-hub-rp-overview).

## Next steps

To try out an end-to-end IoT solution, check out the IoT Hub quickstarts:

* [Quickstart: Send telemetry from a device to an IoT hub](quickstart-send-telemetry-node.md)

To learn more about the ways you can build and deploy IoT solutions with Azure IoT, visit:

* [Fundamentals: Azure IoT technologies and solutions](../iot-fundamentals/iot-services-and-technologies.md).