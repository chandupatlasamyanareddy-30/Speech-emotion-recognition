

<h1>Speech Emotion Recognition using CNNs</h1>
<p>This repository presents an end-to-end pipeline for Speech Emotion Recognition (SER) using Convolutional Neural Networks (CNNs), utilizing the <strong>Toronto Emotional Speech Set (TESS)</strong>.</p>
<h2>Overview</h2>
<ul>
<li>Feature Extraction: MFCCs from raw audio signals</li>
<li>Preprocessing: Spectrogram generation</li>
<li>Model: CNN-based architecture trained for emotion classification</li>
<li>Dataset: Toronto Emotional Speech Set (TESS)</li>
</ul>
<h2>Dataset</h2>
<p><strong>TESS</strong> is a publicly available dataset developed by the University of Toronto. It includes:</p>
<ul>
<li>~2,800 utterances recorded by professional actors</li>
<li>Emotions: Anger, Happiness, Fear, Sadness, Disgust, Surprise, Neutral</li>
<li>High-quality audio recordings (.wav format)</li>
<li>Metadata with speaker information (age, gender)</li>
</ul>
<h2>Installation</h2>
<pre><code>git clone https://github.com/your-username/speech-emotion-cnn.git
cd speech-emotion-cnn
pip install -r requirements.txt</code></pre>
<h2>Usage</h2>
<pre><code># Extract MFCCs and Train the Model
python train.py --dataset_path /path/to/TESS

# Evaluate the Model
python evaluate.py --model_path saved_model.pth

# Predict Emotion from a New Sample
python predict.py --file sample.wav</code></pre>
<h2>Model Architecture</h2>
<ul>
<li>Input: MFCC Spectrograms</li>
<li>3 Convolutional Layers with ReLU and MaxPooling</li>
<li>2 Fully Connected Layers</li>
<li>Softmax Output for 7 Emotion Classes</li>
</ul>
<h2>Training Results</h2>
<h3>Impact of Epochs on Accuracy</h3>
<table>
<tr><th>Epochs</th><th>Time</th><th>Precision</th><th>Accuracy</th></tr>
<tr><td>50</td><td>12s</td><td>0.99</td><td>99%</td></tr>
<tr><td>40</td><td>11s</td><td>0.97</td><td>98.5%</td></tr>
<tr><td>30</td><td>10s</td><td>0.95</td><td>99%</td></tr>
<tr><td>20</td><td>8s</td><td>0.98</td><td>97.5%</td></tr>
<tr><td>10</td><td>7s</td><td>0.97</td><td>98.5%</td></tr>
</table>
<h3>Impact of Validation Split</h3>
<table>
<tr><th>Validation Split</th><th>Time</th><th>Precision</th><th>Accuracy</th></tr>
<tr><td>0.1</td><td>12s</td><td>0.97</td><td>99%</td></tr>
<tr><td>0.2</td><td>11s</td><td>0.99</td><td>98.5%</td></tr>
<tr><td>0.3</td><td>12s</td><td>0.95</td><td>99%</td></tr>
<tr><td>0.4</td><td>17s</td><td>0.98</td><td>97.5%</td></tr>
<tr><td>0.5</td><td>18s</td><td>0.98</td><td>98.5%</td></tr>
</table>
<h2>Visualizations</h2>
<ul>
<li>MFCCs and Spectrograms of audio signals</li>
<li>Model Accuracy vs Epochs</li>
<li>Model Loss vs Epochs</li>
</ul>
<h2>Conclusion</h2>
<p>This project shows the effectiveness of CNNs for Speech Emotion Recognition using audio features like MFCCs. With proper preprocessing, architecture design, and tuning, SER systems can achieve near-human-level accuracy and are suitable for real-world applications such as virtual assistants, customer service bots, and emotion-aware systems.</p>

<h2>Keywords</h2>
<p><strong>Speech Emotion Recognition</strong>, <strong>CNN</strong>, <strong>MFCC</strong>, <strong>TESS</strong>, <strong>Audio Classification</strong>, <strong>Deep Learning</strong></p>
</body>
</html>
