# Audio-Deepfake-Detection

## Part 1: Research & Selection
I explored the [Audio-Deepfake-Detection repo](https://github.com/media-sec-lab/Audio-Deepfake-Detection) and selected three models for detecting AI-generated speech and other audio deepfakes:

### 1. LCNN with Spectrograms

- Innovation: It is a feature based forgery detection. Uses a Lightweight CNN with spectrograms like LFCC to quickly scan audio for spoofing signs.
- Metrics: It gets an EER of about 3.1% on ASVspoof 2019 LA.
- Promise: It is super quick which makes it good for real time needs , and its tested on ASVspoof makes it robust to conversation noise.
- Limitations: It is weaker against modern deepfakes.

### 2. SE-Res2Net-Conformer
- Innovation: it is an end-to-end deep leaening model in this the SE blocks tweaks whats important and then the features are attained by the Res2Net and Conformer then does the end-to-end job.
- Metrics: It gets an  EER of around 1-3% on ASVspoof datasets .
- Promise: It is best in conversation analysis, picks up tricky AI voicesand if optimized or tuned it is good for real-timedetection .
- Limitations: only limitaion is that its a bit complex and is bslow without a GPU.

### 3. RawBoost with CNN
- Innovation: It is an hybrid model where from the raw audio some features are extracted then lets the CNN detect the fake .
- Metrics: It has an EER of about 1.5-2% when used with ASVspoof baselines.
- Promise: Robust for real conversations , the CNN speed suits near real-time and is good for catching AI conversations.
- Limitations: Depends on CNN quality.
