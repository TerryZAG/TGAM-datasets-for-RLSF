# TGAM dataset for RLSF
This dataset was used for the following study:
- [RLSF: Multimodal Sleep Improvement Algorithm based Reinforcement Learning](https://github.com/TerryZAG/RLSF)

## Data-Collection
The TGAM self-made dataset involves 5 subjects aged from 20 to 30. To exhibit diversity, four of these volunteers have healthy sleep status, and the other one has mild symptoms of difficulty falling asleep. Coffee, tea, alcohol, smoking, and sleep-related drugs are restricted within 5 hours before data collection.  
Five recording sessions are performed per subject, and the recording sessions are recorded on the first and second nights without any intervention of white noise. Then, in the three following nights, the white noise lite of each frequency is played in a sequential loop until the end of the set time. Each white noise lite is played one EEG epoch at a time. Since low frequency white noise lite is beneficial to induce sleep, we set  the white noise lite frequencies to 7 kinds, 0Hz, 0.5Hz, 1Hz, 2Hz, 3Hz, 4Hz, and 5Hz, respectively. Starting from lying down, the white noise starts at 0 minutes, 2.5 minutes, and 3 minutes each night.  

## The dataset includes the following:

- Sleep phase EEG of 25 nights for training sleep detection, are located in "data/sleep_stage_data_tgam"
- Data for training TFLSI agent including frequency domain EEG, time domain EEG, frequency domain template EEG and time domain template EEG, are located in "data/tgam_rl_classcial_data"
- Data for training DNSI agent in the simulation environment, including each frequency action EEG, normal sleep EEG，normal sleep template EEG and each frequency template EEG, are located in "data/tgam_rl_DQN_data"

## Sample statistics
Statistics of the TGAM dataset for sleep stage (each sample is a 30-second epoch) are shown as follow:

| Dataset | Subjects | Sample Rate | W | S |
|  ----   |   ----   |     ----    |---|---|
|  TGAM   |     5    |    100Hz    |345|405|

Statistics on the frequency of the TGAM dataset (each sample is a 30-second epoch) are shown as follow:

|           | sleep stage | 0Hz | 0.5Hz | 1Hz | 2Hz | 3Hz | 4Hz | 5Hz |
|  ---      | ----------- | --- | ----- | --- | --- | --- | --- | --- |
|Sample     |      W      | 153 |   28  | 26  | 21  | 21  | 20  | 17  |
|size       |      S      | 222 |   47  | 34  | 39  | 39  | 40  | 43  |

The Statistics of the TGAM dataset with white noise playback start time are as follows:

|                    |  without white noise |  start play at 0 minutes |  start play at 2.5 minutes | start play at 5 minutes |
| ------------------ | --- | --- | --- | --- |
| Number of nights   | 10  |  5  |   5 |   5 |
