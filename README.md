# INDspeech05: INDspeech_NEWS_TTS

This is a speech dataset for developing an Indonesian text-to-speech synthesis system [[Sakti et al., 2008](doc/2008_ssakti_OCOCOSDA.pdf), [Sakti et al., 2010](doc/2010_ssakti_MALINDO.pdf)]. The data was developed by [Advanced Telecommunication Research Institute International (ATR) Japan](https://www.atr.jp/) under the the Asian speech translation advanced research (A-STAR) project [[Sakti et al., 2013](https://www.sciencedirect.com/science/article/pii/S0885230811000404)]. 

## Text and Speech Resources

The raw text source is based on Indonesian daily news and travel expression. We then selected phonetically-balanced sentences from the raw text data, which was assumed to cover almost all phonetic contexts used in the Indonesian language. A total of 2,012 sentences are produced using [the greedy search algorithm](https://www.internationalphoneticassociation.org/icphs-proceedings/ICPhS2003/papers/p15_3145.pdf). The table below shows the number of units and coverage rate.

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

In the original papers [[Sakti et al., 2008](doc/2008_ssakti_OCOCOSDA.pdf), [Sakti et al., 2010](doc/2010_ssakti_MALINDO.pdf)], we define training sets of different sizes; sets with a duration of 12 minutes, 30 minutes, 60 minutes, and 120 minutes (see lst/Orig_trainset_{12min, 30min, 60min, 120min}.lst). For the test set, we have 40 sentences for MOS naturalness (see lst/Orig_testset_MOS.lst) and 20 sentences for SUS intelligibility (see lst/Orig_testset_SUS.lst).

Part of this data has also been used for [Zero Resource Speech Challenge](https://www.zerospeech.com/) [[Dunbar et al. 2019](https://www.isca-speech.org/archive/pdfs/interspeech_2019/dunbar19_interspeech.pdf), [Dunbar et al. 2020](https://www.isca-speech.org/archive_v0/Interspeech_2020/pdfs/2743.pdf)] with different training and test set up (see lst/ZRChallenge_trainset.lst and lst/ZRChallenge_trainset.lst).

## Pronunciation Dictionary

Here we also provide the word list, phoneme list, and pronunciation lexicon (see the word.lst, phoneme.lst, and word_phoneme.lex in lst directory).

The format of the pronunciation dictionary is:
```
WORD PHN_1 PHN_2 ... PHN_N
```
Example:
```
ABAD	A B A D 
ABAIKAN	A B AY K A N 
```

## License

This data is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/) International License (see LICENSE_CC-BY-NC-SA-4.0.txt). You can use the data free for non-commercial purposes, but you have to cite our paper if your work uses our data in your publication. If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original. Furthermore, you are not allowed to create a copy of this dataset and share it publicly in your own repository without our permission.

## Citation

Please cite the following papers:

[[Sakti et al., 2008](doc/2008_ssakti_OCOCOSDA.pdf)]
```
@inproceedings{sakti-tts-cocosda-2008,
    title = "Development of HMM-based Indonesian Speech Synthesis",
    author = "Sakti, Sakriani and Maia, Ranniery and Sakai, Shinsuke and Nakamura, Satoshi",
    booktitle = "Proc. Oriental COCOSDA",
    year = "2008",
    pages = "215--220"
    address = "Kyoto, Japan"
}
```

[[Sakti et al., 2010](doc/2010_ssakti_MALINDO.pdf)]
```
@inproceedings{sakti-tts-malindo-2010,
    title = "Quality and Intelligibility Assessment of Indonesian HMM-Based Speech Synthesis System",
    author = "Sakti, Sakriani and Sakai, Shinsuke and Isotani, Ryosuke and Kawai, Hisashi and Nakamura, Satoshi",
    booktitle = "Proc. MALINDO",
    year = "2010",
    pages = "51--57"
    address = "Jakarta, Indonesia"
}
```

[[Sakti et al., 2013](https://www.sciencedirect.com/science/article/pii/S0885230811000404)]
```
@article{sakti-s2st-csl-2013,
    title = "{A-STAR}: Toward Tranlating Asian Spoken Languages",
    author = "Sakti, Sakriani and Paul, Michael and Finch, Andrew and Sakai, Shinsuke and Thang, Tat Vu, and Kimura, Noriyuki 
    and Hori, Chiori and Sumita, Eiichiro and Nakamura, Satoshi and Park, Jun and Wutiwiwatchai, Chai and Xu, Bo and Riza, Hammam 
    and Arora, Karunesh and Luong, Chi Mai and Li, Haizhou",
    journal = "Special issue on Speech-to-Speech Translation, Computer Speech and Language Journal",
    volume = "27",
    number ="2",
    pages = "509--527",
    year = "2013",
    publisher = "Elsevier"
}
```
