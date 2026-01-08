# Olfactory-Perception-and-EEG-Signal-Correlation
Implement an EEG analysis pipeline to examine neural responses to olfactory stimulation (Lemon vs Rose) across three cognitive groups:
  * Healthy Elderly (Normal)
  * Mild Cognitive Impairment (MCI)
  * Alzheimer’s Disease (AD)
The analysis explores band-specific power differences, statistical effects, and group comparisons.
## Dataset:
The dataset used in this project is publicly available on Mendeley Data and contains EEG recordings collected during an olfactory oddball task. https://data.mendeley.com/datasets/sgzbgwjfkr/5

## Key Features:
* Participants:
  35 older adults including:
  * 15 Healthy (Normal)
  * 7 MCI
  * 13 AD
  (6 initial subjects excluded due to EEG recording issues or medical history)
* Task:
 Participants received a randomized sequence of two odors:
  * Lemon (frequent; 75%)
  * Rose (infrequent; 25%)
The sequence and presentation order are the same for all participants, forming a standard/deviant experimental design. 

## Preprocessing:
*	Average trials per odor
* Bandpass filtering (0.5–40 Hz)
* Use mne.RawArray for processing

## Band Power Extraction:
Estimates spectral power in standard EEG frequency bands:
<br>Band	Frequency
<br>Delta	1–4 Hz
<br>Theta	4–8 Hz
<br>Alpha	8–13 Hz
<br>Beta	13–30 Hz
<br>Gamma	30–40 Hz

## Statistical Tests:
Within-Group
* Paired t-test between Lemon & Rose
* Cohen’s d for effect size
  
Between-Group
* One-way ANOVA across Normal, MCI, and AD for each odor

## Results:
<p align="justify">
Effect sizes (Cohen’s d) were computed to quantify the magnitude of EEG power differences between the Lemon and Rose odor conditions across frequency bands and participant groups (Normal, MCI, and AD). In the Normal group, effect sizes were uniformly small across all frequency bands, indicating minimal neural modulation by odor condition. Similarly, the AD group exhibited consistently small-to-moderate negative effect sizes across bands, suggesting limited responsiveness to olfactory stimulation.
In contrast, the MCI group demonstrated a distinct frequency-specific pattern. While Delta and Alpha bands showed small effects, the Theta band exhibited a moderate negative effect size, indicating relatively greater power under the Rose condition. Notably, higher-frequency bands showed stronger and directionally opposite effects: the Beta band displayed a moderate positive effect size, and the Gamma band exhibited the largest positive effect size across all group–band combinations, reflecting increased power during Lemon exposure. These higher-frequency effects were statistically significant (p < 0.05), whereas lower-frequency band effects did not survive significance testing. Overall, these findings indicate that odor-related EEG modulation was most pronounced in the MCI group and was primarily expressed in higher-frequency oscillatory activity.
</p>

