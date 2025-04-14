# 🌦️ Weather API Azure Function
![Azure Functions](https://img.shields.io/badge/Azure%20Functions-0062AD?style=for-the-badge&logo=azure-functions&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Setup and Configuration](#setup-and-configuration)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Security](#security)

## 🎯 Overview
This Azure Function app fetches real-time weather data from WeatherAPI.com and streams it to Azure Event Hub. The function runs on a timer trigger every 30 seconds, collecting current weather conditions, forecasts, and weather alerts for specified locations.

## ✨ Features
- 🕒 Timer-triggered execution (every 30 seconds)
- 🌡️ Real-time weather data collection
- 📊 Air quality monitoring
- ⚡ Weather alerts tracking
- 🔮 3-day weather forecast
- 🔄 Azure Event Hub integration
- 🔐 Secure credentials management using Azure Key Vault

## 🏗️ Architecture
```mermaid
graph LR
    A[Timer Trigger] --> B[Azure Function]
    B --> C[WeatherAPI.com]
    C --> B
    B --> D[Azure Event Hub]
    B <--> E[Azure Key Vault]
