# TageNet: Urban Traffic Prediction

A deep learning project utilizing Temporal Convolutional Network (TCN) and Transformer architecture to predict traffic congestion in urban areas using real-world traffic data.

## 🎯 Project Overview

This project addresses the critical challenge of urban traffic prediction by implementing a hybrid deep learning architecture combining:

- **Temporal Convolutional Networks (TCN)**: For capturing temporal dependencies in traffic patterns
- **Transformer Architecture**: For learning complex spatial-temporal correlations

The model is trained and evaluated on real-world urban traffic data to predict future traffic congestion levels and assist in traffic management and urban planning.

### Key Features

- Real-world traffic dataset integration
- Hybrid TCN-Transformer architecture
- Temporal and spatial feature learning
- Urban traffic congestion prediction
- Scalable solution for multiple traffic networks

## 🏗️ Architecture

### TCN-Transformer Hybrid Model

The TageNet architecture combines two powerful deep learning paradigms:

**Temporal Convolutional Network (TCN)**
- Captures sequential temporal patterns in traffic flows
- Uses dilated convolutions for extended receptive fields
- Efficient parallel processing of temporal sequences

**Transformer Module**
- Multi-head self-attention mechanisms for spatial relationships
- Positional encoding for traffic network topology
- Cross-temporal attention for long-range dependencies

This hybrid approach enables the model to:
1. Learn temporal dynamics from historical traffic data
2. Capture spatial correlations between different road segments
3. Predict future traffic states with improved accuracy

## 📊 Dataset

### Dataset Description

The project uses a **real-world urban traffic dataset** comprising:

- **Traffic Flow Data**: Hourly/minutely traffic volume measurements
- **Spatial Scope**: Urban road network with multiple intersections and segments
- **Temporal Scope**: Continuous time-series observations spanning extended periods
- **Features**: Traffic speed, volume, occupancy, and congestion indicators

### Dataset Characteristics

| Property | Details |
|----------|---------|
| **Type** | Spatio-temporal time series |
| **Frequency** | Multiple observations per hour |
| **Features** | Traffic flow metrics across network nodes |
| **Temporal Length** | Extended historical period for training and testing |
| **Spatial Coverage** | Urban traffic network graph |

### Data Sources & Attribution

The dataset represents typical urban traffic networks with characteristics from real-world traffic monitoring systems. For specific dataset attribution, source information, and usage guidelines, please refer to the Jupyter notebook: `Urban Traffic Prediction.ipynb`

### Data Preprocessing

- **Normalization**: Min-max scaling or standardization of traffic metrics
- **Temporal Sampling**: Consistent time-interval observations
- **Missing Values**: Handling of sparse or incomplete measurements
- **Train-Test Split**: Chronological split for time-series validation

## 🚀 Installation

### Prerequisites

- Python 3.7 or higher
- Jupyter Notebook
- Dependencies listed in requirements

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/anjishnusaw91/TageNet_Urban-Traffic-Prediction.git
cd TageNet_Urban-Traffic-Prediction
```
2. Install required packages:
```
pip install -r requirements.txt
```
3. Open and run the Jupyter notebook:
```
jupyter notebook "Urban Traffic Prediction.ipynb"
```

## Usage
Running the Model
Execute the cells in the Urban Traffic Prediction.ipynb notebook in sequential order:

1. Data Loading & Exploration: Import and visualize traffic data
2. Data Preprocessing: Normalize and prepare data for model training
3. Model Architecture Definition: Build TCN-Transformer model
4. Model Training: Train on historical traffic data
5. Evaluation: Assess performance on test set
6. Prediction: Generate future traffic predictions

## Example Prediction
```
# Load trained model
model = load_model('traffic_prediction_model.h5')

# Prepare input data (last 24 hours of traffic data)
input_data = prepare_traffic_data(recent_traffic)

# Generate predictions for next 24 hours
predictions = model.predict(input_data)

# Visualize results
plot_predictions(predictions)
```

## 🔬 Model Details

### Input Features
- Historical traffic volume and speed measurements  
- Temporal features (hour of day, day of week, season)  
- Road network topology information  

### Output
- Predicted traffic congestion level for future time steps  
- Confidence intervals or probability distributions for predictions  

### Hyperparameters
- **Sequence Length** – Number of historical time steps used as input  
- **Prediction Horizon** – Number of future time steps to forecast  
- **TCN Channels** – Feature dimensions within convolutional layers  
- **Attention Heads** – Number of parallel attention mechanisms in the Transformer  
- **Batch Size** – Number of samples processed per training iteration  
- **Learning Rate** – Step size for parameter updates during optimization  

### Training Configuration
- **Optimizer:** Adam (or similar adaptive learning rate optimizer)  
- **Loss Function:** Mean Squared Error (MSE) or Mean Absolute Error (MAE)  
- **Epochs:** Number of full passes through the training dataset  
- **Validation Split:** Percentage of dataset reserved for validation  


---

## 📈 Results

The **TageNet** model demonstrates improved performance in urban traffic prediction through a hybrid architecture combining **Temporal Convolutional Networks (TCN)** and **Transformer attention mechanisms**.

Key advantages include:

- **Temporal Modeling**  
  The TCN architecture captures traffic dynamics across multiple time scales, enabling effective modeling of short-term and long-term temporal dependencies.

- **Spatial Correlation Learning**  
  Transformer attention layers learn relationships between different road segments, capturing complex spatial dependencies.

- **Improved Prediction Accuracy**  
  The combined architecture reduces forecasting errors compared to conventional baseline models.

For detailed evaluation metrics, experimental results, and visualizations, refer to the output cells in the **Jupyter Notebook** provided in this repository.


---

## 🤝 Contributing

Contributions are welcome and encouraged.

To contribute:

1. Fork the repository
2. Create a new feature branch
   ```bash
   git checkout -b feature/improvement
   ```
3. Commit your changes
   ```bash
   git commit -m "Add improvement"
   ```
4. Push to your branch
   ```bash
   git push origin feature/improvement
   ```
5. Open a Pull Request


---

## 📧 Contact

**Author:** anjishnusaw91  

**Repository:** TageNet_Urban-Traffic-Prediction  

**Last Updated:** March 8, 2026  


---

## 🔗 References

### Key Concepts

- **Temporal Convolutional Networks**  
  Lea et al., *"Temporal Convolutional Networks for Action Segmentation and Detection"* (2017)

- **Transformers**  
  Vaswani et al., *"Attention is All You Need"* (2017)

- **Traffic Prediction**  
  Research from spatio-temporal forecasting and urban computing literature


### Related Work

For additional insights into traffic forecasting models, explore research involving:

- Graph Neural Networks (GNNs) for traffic flow prediction  
- LSTM-based sequence-to-sequence traffic forecasting models  
- Attention-based architectures for spatio-temporal prediction  


---

## ⚠ Disclaimer

For dataset-specific citations, licensing details, and source attribution, please refer to the **primary Jupyter Notebook** and any accompanying documentation included in this repository.
