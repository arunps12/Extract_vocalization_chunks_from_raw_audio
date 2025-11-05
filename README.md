
# Extract_vocalization_chunks_from_raw_audio

## Prerequisites

Ensure you have the following installed:
- Python 3.10.5

## Requirements

First, to install the required Python packages, use the provided `install_requirements.py` script.

### Installing Requirements

1. Ensure you have `pip` installed.
2. Run the following command to install the required packages:
   ```sh
   python install_requirements.py
   ```
Then you need to run the script named `extracting_voc_chunks_metadata.py` designed to extract vocalization chunks from raw audio recordings and generate a metadata CSV file. The raw audio data is sourced from the [Infant and Adult Vocalizations in Home Audio Recordings dataset](https://figshare.com/articles/dataset/Infant_and_adult_vocalizations_in_home_audio_recordings/6108392), which is open source and provides both the raw audio and the timings of each vocalization chunk in corresponding text files.

The `extracting_voc_chunks_metadata.py` script performs the following tasks:
1. Reads the raw audio files and their corresponding timing text files.
2. Extracts vocalization chunks from the raw audio based on the provided timings.
3. Saves the extracted chunks into a specified directory.
4. Generates a metadata CSV file with the file names of the extracted chunks and their labels.
To run the script, run it from the command line with three string inputs specifying the directories for the raw audio, the output directory for vocalization chunks, and the metadata directory.

```sh
python extracting_voc_chunks_metadata.py <raw_audio_dir> <voc_chunks_dir> <metadata_dir>
```
## Script Details
The script performs the following steps:

1. Loading Raw Audio and Timings: Reads the raw audio files and their corresponding timing text files from the specified directory.
2. Extracting Vocalization Chunks: Uses the timing information to extract vocalization chunks from the raw audio files.
3. Saving Extracted Chunks: Saves each extracted chunk as a separate audio file in the specified vocalization chunks directory.
4. Generating Metadata: Creates a metadata CSV file with two columns: the file name of each extracted chunk and its label.

### Example Directory Structure
```sh
project_root/
├── install_requirements.py
├── extracting_voc_chunks_metadata.py
├── requirements.txt
├── raw_audio_dir/
│   ├── example1.wav
│   ├── example1.txt
|   ├── example2.wav
│   ├── example2.txt
│   └── ...
└── voc_chunks_dir/
└── out_dir/
```
---
## 🌟 About Me

Hi there! I'm **Arun Prakash Singh**, a **Marie Curie Research Fellow at the University of Oslo (UiO)**.  
My research focuses on **speech technology, data engineering, and machine learning**, with an emphasis on building intelligent, data-driven systems that model human communication and learning.  
I am passionate about integrating **AI, analytics, and large-scale data pipelines** to advance our understanding of how humans process and acquire language.
