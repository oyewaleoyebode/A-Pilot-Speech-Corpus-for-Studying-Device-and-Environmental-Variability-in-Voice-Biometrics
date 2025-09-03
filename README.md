# A-Pilot-Speech-Corpus-for-Studying-Device-and-Environmental-Variability-in-Voice-Biometrics

## Abstract 

This paper introduces a curated speech dataset developed to support research in speech enhancement and robust voice biometric verification. 

The dataset addresses the critical challenge of voice variability across devices and environments, which can significantly reduce the reliability of speaker verification systems in real-world applications such as mobile banking.

A total of 480 recordings were collected from 12 participants with diverse demographic backgrounds, including individuals from Japan, Nigeria, the Ivory Coast, France, Germany, and Indonesia. 

Each participant contributed 40 utterances, recorded across multiple devices: Samsung A04s, OnePlus Nord, iPhone 15 Pro, and a USB condenser microphone on a MacBook, and under both indoor and outdoor conditions. The recordings capture variations introduced by microphone quality, network transmission (in-call speech), and environmental noise. 

All files are stored in WAV format with standardized sampling rates between 8–16 kHz, accompanied by metadata containing non-identifiable demographic attributes such as nationality, age, gender, and English proficiency.

The dataset is designed for evaluating and benchmarking speech enhancement algorithms, including spectral subtraction, Wiener filtering, and adaptive filtering, as well as for studying their impact on downstream speaker identification and verification tasks. 

By providing a balanced collection of cross-device, cross-environment recordings, this dataset enables the development of more consistent, accurate, and secure voice biometric systems.

## Value of the Data

- Benchmark resource for speech biometrics: The dataset captures cross-device, cross-environment variability that is underrepresented in existing corpora like VoxCeleb or LibriSpeech.
-	Practical relevance: Collected with everyday devices (low- to high-end smartphones, in-call channels), reflecting real-world conditions faced in mobile banking authentication.
-	Security applications: Supports robustness testing, spoofing resilience, and liveness detection research.
-	Low-resource settings: Valuable for studies where large datasets are unavailable, providing a pilot-scale corpus for transfer learning and comparative evaluation.
-	Reusability: Organized with speaker-wise folders and metadata files for easy integration into machine learning pipelines.


### Audio files (.wav)
- 12 anonymized speaker folders (`speaker_01`, `speaker_02`, …)  
- Each folder contains ~40 utterances  
- Sampling rates: **8–16 kHz**, 16-bit PCM  
- File naming: `audio_1.wav`, `audio_2.wav`, …  

**Data Format**
- The main fields per entry in the dataset are: **Participant ID, Nationality, English Proficiency, Age, Gender, Status**.
- The data is available in both **.csv** and **.JSON** formats. 

Below is an example of an entry from our dataset:
```
    {
        "participant_id":"ZVMKSJ",
        "nationality":"Indonesia",
        "english_proficiency":"Basic",
        "age":38.0,
        "gender":"Male",
        "status":"present"
    }
```
---

## Recording Setup
### Devices
-	Samsung A04s, OnePlus Nord (in-call mode): Captured speech transmitted through cellular networks, including the effects of compression, packet loss, and channel distortion.
-	Samsung A04s, OnePlus Nord (direct recordings): Representative mid-range Android smartphones commonly used in developing regions, providing insights into differences in built-in microphone quality and processing pipelines.
- iPhone 15 Pro: A high-end smartphone with advanced microphone arrays and noise reduction algorithms, designed to contrast with mid-range devices and capture premium consumer hardware performance.
-	USB condenser microphone (MacBook): Provided near-studio quality reference recordings, serving as an upper 
 

### Environments
Two environments were included to simulate real-world usage:
- Indoor recordings: Collected in the NAIST Building A lobby, a semi-controlled environment with background activity such as footsteps and conversations.
- Outdoor recordings: Captured in campus surroundings, incorporating natural noise sources such as wind, traffic, and crowd movement.


## License
This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.  
You are free to **use, share, and adapt** the dataset with appropriate attribution.  


### Related publication
O. O. Oyewale, M. D. Hossain, Y. Taenaka, and Y. Kadobayashi, *Optimizing Voice Biometric Verification in Banking with Machine Learning for Speaker Identification*, Proc. 2024 IEEE 29th Asia Pacific Conf. on Communications (APCC), pp. 377–384, doi: [10.1109/APCC62576.2024.10768085](https://doi.org/10.1109/APCC62576.2024.10768085).
 
**View Repository: https://github.com/oyewaleoyebode/Optimizing-Voice-Biometric-Verification-in-Banking-with-Machine-Learning-for-Speaker-Identification**


## Download the Dataset
The dataset is available on **Hugging Face**:  
👉 [https://huggingface.co/datasets/Oye12/A_Pilot_Speech_Corpus](https://huggingface.co/datasets/Oye12/A_Pilot_Speech_Corpus)


---
## Citation
If you use this dataset, please cite the following:

```bibtex
@dataset{oyewale_2025_figshare,
  author       = {Oyebode Oluwatobi Oyewale},
  title        = {A Pilot Speech Corpus for Studying Device and Environmental Variability in Voice Biometrics},
  year         = {2025},
  publisher    = {Figshare},
  doi          = {10.6084/m9.figshare.30039037},
  url          = {https://doi.org/10.6084/m9.figshare.30039037}
}
```
