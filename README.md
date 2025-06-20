# Telecom Customer Churn Prediction

## Описание проекта

**Telecom Customer Churn Prediction** — проект по построению модели для прогнозирования оттока клиентов телеком-оператора «ТелеДом». Цель — выявить клиентов, которые могут расторгнуть договор, чтобы вовремя предложить им специальные условия и промокоды и тем самым уменьшить отток.

## Данные

В проекте используются следующие таблицы из базы данных:

- **contract** — сведения о договорах:
  - `customerID` — уникальный идентификатор клиента
  - `BeginDate`, `EndDate` — даты начала и окончания действия договора
  - `Type` — тип оплаты (ежемесячно/год и более)
  - `PaperlessBilling` — электронный расчетный лист
  - `PaymentMethod` — способ оплаты
  - `MonthlyCharges`, `TotalCharges` — ежемесячные и суммарные расходы

- **personal** — персональные данные:
  - `customerID` — уникальный идентификатор клиента
  - `gender` — пол
  - `SeniorCitizen` — пенсионер или нет
  - `Partner` — наличие супруга(и)
  - `Dependents` — наличие детей

- **internet** — данные по интернет-услугам:
  - `customerID`
  - `InternetService` — тип подключения
  - `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies` — наличие соответствующих услуг

- **phone** — данные по телефонным услугам:
  - `customerID`
  - `MultipleLines` — подключение к нескольким линиям

## Цель

Обучить и внедрить модель, способную предсказывать вероятность расторжения договора клиентом (`churn`). Это поможет вовремя выявлять "уходящих" клиентов и предлагать им удерживающие меры.

## Используемые библиотеки

- pandas, numpy, matplotlib, seaborn — анализ и визуализация данных
- scikit-learn — препроцессинг, обучение моделей, метрики
- catboost — градиентный бустинг для задач классификации
- optuna — автоматический подбор гиперпараметров
- torch — нейронные сети
- phik — корреляционный анализ категориальных признаков
- sqlalchemy — работа с базой данных
