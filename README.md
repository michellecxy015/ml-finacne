Financial Forecasting with Neural Networks

This repository contains experiments applying various deep learning architectures to predict financial market returns based on macroeconomic and market indicators. It includes implementations of:

- **DNN** (Deep Neural Networks)
- **CNN** (Convolutional Neural Networks)
- **RNN/LSTM** (Recurrent Neural Networks with Long Short-Term Memory)
- **Autoencoders** (AE, CAE, VAE)

## 📁 Project Structure
├── AE, CAE, VAE.ipynb       # Autoencoder experiments

├── cnn.ipynb                # CNN model for time series forecasting

├── dnn.ipynb                # DNN experiments

├── rnn_new (1).ipynb        # RNN/LSTM experiments

├── market_data.xlsx         # Macroeconomic + financial time series dataset

├── README.md                # Project overview and documentation
## 📊 Dataset

The file `market_data.xlsx` includes 17 macroeconomic and financial signals such as:

- GDP, CPI, M2, Unemployment (UN)
- Short-term and long-term rates (Y02, Y10)
- Interest rate spreads (STP, IR, RR)
- Asset prices and sentiment indicators: Oil (`_OIL`), Gold (`_AU`), Dollar Index (`_DXY`), Large Cap (`_LCP`), Treasuries (`_TY`)

The target variable is `'_MKT'`, representing future market returns.

## 📈 Model Overview

| Notebook         | Model Type        | Description                                   |
|------------------|-------------------|-----------------------------------------------|
| `dnn.ipynb`      | Fully connected DNN | Baseline model using standardized inputs      |
| `cnn.ipynb`      | CNN (1D)          | Temporal pattern recognition from windows     |
| `rnn_new (1).ipynb` | LSTM-RNN        | Sequence modeling of macro-financial signals  |
| `AE, CAE, VAE.ipynb` | Autoencoders  | Dimensionality reduction + unsupervised setup |

## ⚙️ Requirements

All experiments are implemented in Python using:

- `TensorFlow` / `Keras`
- `pandas`, `numpy`, `scikit-learn`
- `matplotlib`
  
🧪 Experiment Strategy
	•	All models are evaluated on combinations of 2–4 input signals.
	•	A sliding-window training scheme is used (e.g., 5-step input → 1-step forecast).
	•	Models are evaluated using:
	•	Validation loss (MSE for regression, binary cross-entropy for classification)
	•	Correlation (IC)
	•	Sharpe Ratio (for trading strategy simulation)

  ## License

This project is for educational and research use. For commercial inquiries, please contact the maintainers.
