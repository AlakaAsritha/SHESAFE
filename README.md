# SheSafe
### AI-Based SOS Communicator with Speech Stress & Motion Anomaly Detection

SafeShe is an AI-powered Android application designed to enhance women's safety by automatically detecting distress situations using speech stress analysis and motion anomaly detection. The system works in real time and sends SOS alerts without requiring manual intervention.



## Project Overview

In emergency situations, victims may not always be able to manually trigger an SOS alert. SafeShe addresses this problem by continuously monitoring:
- **Speech stress levels** using deep learning
- **Motion anomalies** using smartphone sensors

When abnormal patterns are detected, the system automatically sends an SOS message to predefined emergency contacts.



## Objectives

- Detect stress in human speech using deep learning models
- Identify abnormal physical movements such as sudden falls or unusual activity
- Automatically trigger SOS alerts via SMS
- Implement the complete solution as an Android mobile application



## System Architecture

### Speech Stress Detection
- **Dataset:** RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)
- **Feature Extraction:** Mel-Frequency Cepstral Coefficients (MFCC)
- **Model Used:** LSTM (Long Short-Term Memory)
- **Output:** Classification of speech into emotional categories to identify stress

### Motion Anomaly Detection
- **Dataset:** MobiAct Dataset
- **Sensors Used:** Accelerometer & Gyroscope
- **Feature Extraction:** Mean, variance, peak values, FFT
- **Models Used:**
  - LSTM Autoencoder
  - One-Class SVM
- **Detection Method:** Mean Squared Error (MSE) thresholding



## Android Application Implementation

- Developed using **Android Studio**
- Uses **TensorFlow Lite (TFLite)** for on-device inference
- Continuously monitors sensor data in real time
- Automatically sends SOS alerts via SMS when anomalies are detected

### Key Components:
- **MainActivity**
  - Reads accelerometer and gyroscope data
  - Loads and runs the TFLite model
  - Detects anomalies using MSE threshold
- **AndroidManifest.xml**
  - Manages permissions (SMS, sensors)
  - Defines app entry points and configuration
- **Gradle Build System**
  - Ensures compatibility with Android SDK 35
  - Manages dependencies and project structure



## Technologies Used

- Python (Model training)
- TensorFlow / TensorFlow Lite
- LSTM, LSTM Autoencoder, One-Class SVM
- Android Studio
- Java / Kotlin
- MFCC Feature Extraction
- Smartphone Sensors (Accelerometer & Gyroscope)



## Results

- Successfully detects abnormal motion and distress patterns
- Automatically sends SOS messages during emergency situations
- Demonstrates reliable real-time performance on mobile devices



## Applications

- Women safety systems
- Personal emergency response systems
- Smart healthcare monitoring
- AI-driven mobile safety applications



## Conclusion

SafeShe demonstrates the effective use of AI, sensor technology, and mobile communication to create a proactive personal safety solution. The project highlights how intelligent systems can assist in real-world emergency scenarios, especially for enhancing women’s safety.



## Future Enhancements

- Live location sharing with SOS alerts
- Integration with emergency services
- Cloud-based alert monitoring
- Multilingual speech stress detection



## License

This project is developed for academic and research purposes.
