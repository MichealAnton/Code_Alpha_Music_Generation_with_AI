# Code_Alpha_Music_Generation_with_AI
An AI model that uses RNN architecture with LSTM layers and trained on MIDI files from Classical MIDI dataset from Kaggle


## Features

- MIDI file parsing and preprocessing
- LSTM-based sequence modeling for music generation
- Controllable output length
- Visual sheet music display
- Audio playback directly in the notebook
- MIDI file export capability

## Requirements

- Python 3.7+
- Kaggle account (for dataset access)
- Required packages:
    music21
    tensorflow  
    numpy
    kagglehub
## Installation

1. Clone this repository
2. Install dependencies:
 ```bash
 pip install music21 tensorflow numpy kagglehub
 sudo apt-get install -y lilypond


# Dataset
The model uses the Classical Music MIDI dataset from Kaggle, specifically the Mozart subdirectory.

## Code Structure
Data loading and preprocessing
Model architecture definition
Training pipeline
Music generation functions
Visualization and playback utilities

## How to Use
Training the Model
Run the notebook cells in sequence

The model will automatically:
Download the dataset
Preprocess the MIDI files
Train the LSTM network
Save the best model checkpoint

## Generating Music
Use the generate_and_play() function with parameters:

generate_and_play(
    start_sequence=None,  # Optional starting sequence
    length=200           # Number of notes to generate
)

# Output
The function will:

Generate the musical sequence

Display the sheet music

Play the audio

Save a MIDI file named generated_music.mid

# Model Architecture
3 LSTM layers (512 units each)

Dropout and Batch Normalization

Dense layers with ReLU and Softmax activations

Sequence length: 100 notes

Vocabulary size: Based on unique notes in dataset

# Training Parameters
Batch size: 128

Epochs: 50

Optimizer: Adam

Loss: Categorical Crossentropy

Validation split: 20%

# Customization
You can modify:

sequence_length in the preparation code

Model architecture in create_model()

Training parameters in the model.fit() call

Generation parameters in generate_and_play()

# Limitations
Generation quality depends on training data

Longer sequences may lose coherence

Requires significant computational resources for training

# Future Improvements
Add temperature parameter for generation

Implement attention mechanisms

Add chord progression constraints

Incorporate musical theory rules


