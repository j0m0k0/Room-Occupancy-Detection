# Room Occupancy Prediction

This repository contains the code and documentation for the project "Room Occupancy Prediction using Environmental Observations" for the Deep Learning course at Texas State University.

## Project Overview

This project utilizes a dataset to predict room occupancy using environmental observations such as temperature, humidity, and CO2 levels. Effective prediction of occupancy from such data can significantly enhance the efficiency of energy usage in buildings and improve automated system responses to human presence.

We have implemented five different models to address this problem:
- RandomForest Classifier
- Multilayer Perceptron (MLP)
- Convolutional Neural Network (CNN)
- Long Short-Term Memory Network (LSTM)
- Transformer

## Authors

- Javad Mokhtari Koushyar ([koushyar@txstate.edu](mailto:koushyar@txstate.edu))
- Bao Hoang Duc Vo ([bao.vo@txstate.edu](mailto:bao.vo@txstate.edu))

## Dataset

The dataset used in this project is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection). It comprises several environmental attributes collected from sensors:

- **Date**: Records the exact date and time of the data entry.
- **Temperature**: Indicates the ambient temperature of the environment.
- **Relative Humidity**: Shows the amount of moisture in the air.
- **Light**: Represents the light level of the environment.
- **CO2**: Can indicate human occupancy and affect the perceived air quality.
- **Humidity Ratio**: Useful for understanding the air’s capacity to hold moisture.
- **Occupancy**: This is the target variable for prediction.

## Methods and Models

### 1. RandomForest Classifier
- **Architecture**: Configured with 100 trees and a random state of 42.
- **Training Process**: Model was trained on features including temperature, humidity, light, CO2, and humidity ratio.
- **Evaluation**: Achieved an accuracy of 0.96 on the test set.

### 2. Multilayer Perceptron (MLP)
- **Architecture**: Three linear layers with ReLU activations and dropout layers.
- **Training Process**: Used Adam optimizer and Binary Cross-Entropy loss function over 100 epochs.
- **Evaluation**: Achieved an accuracy of 0.99 on the test set.

### 3. Convolutional Neural Network (CNN)
- **Architecture**: Two 1D convolutional layers followed by max pooling and linear layers.
- **Training Process**: Used Adam optimizer and Binary Cross-Entropy loss function over 100 epochs.
- **Evaluation**: Achieved an accuracy of 0.94 on the test set.

### 4. Long Short-Term Memory Network (LSTM)
- **Architecture**: LSTM layers configured for time-series prediction.
- **Training Process**: Used Adam optimizer and Binary Cross-Entropy loss function over 100 epochs.
- **Evaluation**: Achieved an accuracy of 0.95 on the test set.

### 5. Transformer
- **Architecture**: Encoder and decoder with multiple layers, utilizing MultiheadAttention mechanisms.
- **Training Process**: Employed techniques such as learning rate scheduling and early stopping.
- **Evaluation**: Achieved an accuracy of 0.97 on the test set.

## Results and Discussion

All models demonstrated robust performance in predicting room occupancy, with the Transformer model yielding the highest accuracy. Future improvements could include hyperparameter tuning and expanded training data to enhance generalization and performance.

## Video Presentation
A general presentation of the project can be found at [here](https://www.youtube.com/watch?v=icl6ltTO0Ag&ab_channel=ComputerSciencePh.D.Student).
## Conclusion

This project successfully implemented and evaluated various machine learning models to predict room occupancy based on environmental data. The results indicate the potential for these models to contribute to energy-efficient building management systems.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

We would like to thank Texas State University and the UCI Machine Learning Repository for providing the resources and data necessary for this project.

## Citation

If you use this work, please cite it as follows:

```bibtex
@misc{mokhtarikoushyar2024occupancy,
  title={Room Occupancy Prediction using Environmental Observations},
  author={Javad Mokhtari Koushyar and Bao Hoang Duc Vo},
  year={2024},
  howpublished={\url{https://github.com/your-repo-url}},
  note={Texas State University, Department of Computer Science, Deep Learning Course}
}
