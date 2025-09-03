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

  ## Dataset Contents
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

---

## Validation

- The dataset underwent multiple validation procedures to ensure consistency, usability, and reliability for research in speaker verification and voice biometrics. All audio files were manually inspected to verify correct labeling, completeness, and the absence of distortions such as clipping or truncated speech. Sampling rates and bit depths were standardized to ensure comparability across devices.

- In addition, we evaluated its applicability in speaker identification tasks using three different speech enhancement approaches: spectral subtraction, Wiener filtering, and adaptive filtering. Results showed that the adaptive filter achieved the highest performance, with a 97% success rate, outperforming spectral subtraction (92%) and Wiener filtering (89%). The adaptive filter consistently yielded higher signal-to-noise ratio (SNR) values, lower mean squared error (MSE), and reduced weighted spectral slope (WSS) distortion, effectively reducing background noise while maintaining the naturalness of speech signals.

- These validation results confirm that the dataset captures sufficient variability to challenge baseline models while remaining suitable for robust algorithm development. At the same time, they highlight potential research opportunities in addressing device-induced and environment-induced variations.

- It is important to note that while the adaptive filter offers superior accuracy, it introduces higher computational complexity compared to simpler enhancement techniques. This may limit its suitability for real-time deployment in resource-constrained mobile devices, a challenge that future research should address through optimization techniques or hardware acceleration. Expanding the dataset to include a broader range of speakers and devices, and integrating deep learning–based enhancement and multimodal biometrics, are additional directions that could further strengthen the applicability and generalizability of this resource.


✅ Results confirm the dataset captures sufficient variability to challenge baseline models while supporting robust algorithm development.

---

## Applications
- Benchmarking **speaker identification & verification** models  
- Studying **speech enhancement** under noisy / degraded conditions  
- Exploring **spoofing resilience** and **liveness detection**  
- Transfer learning in **low-resource settings**  

---

### Related publication
O. O. Oyewale, M. D. Hossain, Y. Taenaka, and Y. Kadobayashi, *Optimizing Voice Biometric Verification in Banking with Machine Learning for Speaker Identification*, Proc. 2024 IEEE 29th Asia Pacific Conf. on Communications (APCC), pp. 377–384, doi: [10.1109/APCC62576.2024.10768085](https://doi.org/10.1109/APCC62576.2024.10768085).
 
** View Repository: https://github.com/oyewaleoyebode/Optimizing-Voice-Biometric-Verification-in-Banking-with-Machine-Learning-for-Speaker-Identification **
---

## License
This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.  
You are free to **use, share, and adapt** the dataset with appropriate attribution.  

[https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)

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
