## Overview

This repository provides the PyTorch implementation of **ST-SAGA: Intrinsically Interpretable Spatio-Temporal Bus Passenger Flow Forecasting with Shapley-Guided Additive Group Attribution**, an intrinsically interpretable framework for short-term bus passenger flow forecasting.

ST-SAGA combines route-aware spatio-temporal modeling with Shapley-guided additive prediction decomposition. The framework provides intrinsic group-level attributions and fine-grained explanations of individual bus stops and historical time steps using Owen values.

## Key Components

- **Spatio-temporal encoder:** Route-aware graph convolution, transfer-aware attention, and LSTM-based temporal modeling.
- **Intrinsic additive decomposition:** Prediction contributions across three spatial contexts (self, same-route, transfer) and three temporal windows (old, mid, recent).
- **Shapley-guided alignment:** Alignment of reference-adjusted intrinsic contributions with exact grouped Shapley values.
- **Fine-grained attribution:** Owen-value explanations for individual stops and historical time steps.
- **Experimental evaluation:** Forecasting accuracy, explanation fidelity, and ablation studies.

## Dataset


## Dataset

Experiments are conducted using the **October 2022 data** from the [original Ames Bus Network Dataset](https://drive.google.com/file/d/1zEqDMmPK3IQVmEvcRI4JmpVKeaE_BcFe/view?usp=sharing), following preprocessing to retain 17 bus routes and 515 route-stop nodes. The model forecasts passenger flow for the next 10-minute interval using observations from the preceding 12 intervals (two hours).

