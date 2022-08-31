# INDspeech_NEWS_TTS

This is a speech dataset for developing an Indonesian text-to-speech synthesis system. 

## Text and Speech Resources

The raw text source is based on Indonesian daily news and travel expression. We then selected phonetically-balanced sentences from the raw text data, which was assumed to cover almost all phonetic contexts used in the Indonesian language. A total of 2,012 sentences are produced using the greedy search algorithm. The table below shows the number of units and coverage rate.

|       Phone     | # Units | Coverage | 
| --------------- | ------- |--------- |
| Monophones      |      33 |     100% | 
| Left Biphones   |     814 |   99.75% | 
| Right Biphones  |     813 |   99.75% | 
| Triphones       |    8270 |   85.18% | 

After that, we recorded the speech by a female Indonesian speaker who spoke standard Indonesian (no accent). Each audio file is a single-channel 16-bit PCM WAV with a sample rate of 16000 Hz.

## File Format

"SPK00_F_XXXX" where "SPK00_F" represents the ID of the single female speaker and "XXXX" represents the sentence ID.

## Training and Test Dataset

In the original paper, we define training sets of different sizes; sets with a duration of 12 minutes, 30 minutes, 60 minutes, and 120 minutes (See lst/Orig_trainset_{12min, 30min, 60min, 120min}.lst). For the test set, we have 40 sentences for MOS naturalness (See lst/Orig_testset_MOS.lst) and 20 sentences for SUS intelligibility (See lst/Orig_testset_SUS.lst).

Part of this data has been used for [Zero Resource Speech Challenge](https://www.zerospeech.com/) with different training and test set up (See lst/ZRChallenge_trainset.lst and lst/ZRChallenge_trainset.lst).
