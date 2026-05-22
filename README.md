# Emotion Detector Application

An AI-based web application developed using Python, Flask, and the Watson NLP library that analyzes textual data to predict embedded emotions. The application identifies five core emotions: anger, disgust, fear, joy, and sadness, along with the dominant emotion.

## Project Structure
* `EmotionDetection/`: Python package containing the logic for calling the Watson NLP API.
* `server.py`: Flask application server providing the web interface and API endpoints.
* `test_emotion_detection.py`: Unit tests validating the accuracy of the application.

## API Usage
The application utilizes the Watson NLP Emotion Aggregated Workflow to process text dynamically and return formatted JSON structures containing precise emotion scores:

$$I = \text{Score}_{\text{emotion}}$$

### Core Mathematical Analysis
The system computes the maximum confidence score to determine the dominant emotion:
$$\text{Dominant Emotion} = \arg\max_{e} (\text{Score}_e)$$
Where $e \in \{\text{anger}, \text{disgust}, \text{fear}, \text{joy}, \text{sadness}\}$.

## Deployment
Run the local server using:
```bash
python3 server.py
