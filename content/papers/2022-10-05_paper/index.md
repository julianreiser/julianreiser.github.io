---
title: "ECG performance in simultaneous recordings of five wearable devices using a new morphological noise-to-signal index and Smith-Waterman-based RR interval comparisons" 
date: 2022-10-05
tags: ["wearable technology","ECG monitoring","signal quality assessment","heart rate monitoring","mobile physiological monitoring","QRS detection","RR intervals","validation study","comparative analysis","noise-to-signal ratio","morphological analysis","ergonomics","sports science","real-world environments"]
author: ["Dominic Bläsing", "Anja Buder", "Julian Elias Reiser", "Maria Nisser", "Steffen Derlien", "Marcus Vollmer"]
description: "A comprehensive comparison of five ECG wearable devices tested simultaneously in realistic use scenarios including cognitive and physical tasks. The study introduces novel signal quality assessment methods including morphological noise-to-signal ratio (morphSQ) and Smith-Waterman-based RR interval validation for evaluating device performance across different activity levels."
summary: "This study evaluated five ECG devices (eMotion Faros 360°, Hexoskin Hx1, NeXus-10 MKII, Polar RS800 Multi, and SOMNOtouch NIBP) worn simultaneously by 13 participants during rest, walking, cognitive tasks, and uphill running. A novel morphological signal quality index (morphSQ) and modified Smith-Waterman algorithm were developed to assess signal quality and RR interval accuracy. Results showed all devices achieved sufficient quality during non-movement conditions, with eMotion Faros 360° demonstrating the most stable performance across all conditions, while movement-related artifacts affected devices differently based on their design and electrode placement."
cover:
    image: "2022-10-05_ecg_wearable_comparison.png"
    alt: "Five ECG wearable devices simultaneous recording setup"
    relative: true
editPost:
    URL: "https://doi.org/10.1371/journal.pone.0274994"
    Text: "PLOS ONE"

---

---

##### Links

+ [Full Paper](https://doi.org/10.1371/journal.pone.0274994)

---

##### Abstract

**Background:** Numerous wearables are used in a research context to record cardiac activity although their validity and usability has not been fully investigated. The objectives of this study is the cross-model comparison of data quality at different realistic use cases (cognitive and physical tasks). The recording quality is expressed by the ability to accurately detect the QRS complex, the amount of noise in the data, and the quality of RR intervals.

**Methods:** Five ECG devices (eMotion Faros 360°, Hexoskin Hx1, NeXus-10 MKII, Polar RS800 Multi and SOMNOtouch NIBP) were attached and simultaneously tested in 13 participants. Used test conditions included: measurements during rest, treadmill walking/running, and a cognitive 2-back task. Signal quality was assessed by a new local morphological quality parameter morphSQ which is defined as a weighted peak noise-to-signal ratio on percentage scale. The QRS detection performance was evaluated with eplimited on synchronized data by comparison to ground truth annotations. A modification of the Smith-Waterman algorithm has been used to assess the RR interval quality and to classify incorrect beat annotations.

**Results:** All used devices achieved sufficient signal quality in non-movement conditions. Over all experimental phases, insufficient quality expressed by morphSQ values below 10% was only found in 1.22% of the recorded beats using eMotion Faros 360° whereas the rate was 8.67% with Hexoskin Hx1. Nevertheless, QRS detection performed well across all used devices with positive predictive values between 0.985 and 1.000. False negative rates are ranging between 0.003 and 0.017. eMotion Faros 360° achieved the most stable results among the tested devices with only 5 false positive and 19 misplaced beats across all recordings identified by the Smith-Waterman approach.

**Conclusion:** Data quality was assessed by two new approaches: analyzing the noise-to-signal ratio using morphSQ, and RR interval quality using Smith-Waterman. Both methods deliver comparable results. However the Smith-Waterman approach allows the direct comparison of RR intervals without the need for signal synchronization whereas morphSQ can be computed locally.

---

##### Citation

Bläsing, D., A. Buder, J. E. Reiser, M. Nisser, S. Derlien, and M. Vollmer. 2022. "ECG performance in simultaneous recordings of five wearable devices using a new morphological noise-to-signal index and Smith-Waterman-based RR interval comparisons." PLOS ONE 17(10): e0274994. https://doi.org/10.1371/journal.pone.0274994.

```BibTeX
@article{blaesing2022ecg,
author = {Bläsing, Dominic and Buder, Anja and Reiser, Julian Elias and Nisser, Maria and Derlien, Steffen and Vollmer, Marcus},
title = {ECG performance in simultaneous recordings of five wearable devices using a new morphological noise-to-signal index and Smith-Waterman-based RR interval comparisons},
journal = {PLOS ONE},
volume = {17},
number = {10},
pages = {e0274994},
year = {2022},
month = {October},
doi = {10.1371/journal.pone.0274994},
url = {https://doi.org/10.1371/journal.pone.0274994},
abstract = {Numerous wearables are used in a research context to record cardiac activity although their validity and usability has not been fully investigated. The objectives of this study is the cross-model comparison of data quality at different realistic use cases (cognitive and physical tasks). The recording quality is expressed by the ability to accurately detect the QRS complex, the amount of noise in the data, and the quality of RR intervals. Five ECG devices were attached and simultaneously tested in 13 participants during rest, treadmill walking/running, and a cognitive 2-back task. Signal quality was assessed by a new local morphological quality parameter morphSQ and QRS detection performance was evaluated using a modification of the Smith-Waterman algorithm for RR interval quality assessment.}
}
```