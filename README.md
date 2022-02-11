# Deep Performer: Score-to-audio music performance synthesis

Deep Performer is a novel three-stage system for score-to-audio music performance synthesis. It is based on a transformer encoder-decoder architecture commonly used in text-to-speech synthesis. In order to handle polyphonic music inputs, we propose a new _polyphonic mixer_ for aligning the encoder and decoder. Moreover, we propose a new _note-wise positional encoding_ for providing a fine-grained conditioning to the model so that the model can learn to behave differently at the beginning, middle and end of a note.

## Dataset

We used two datasets to train our proposed system: [Bach Violin Dataset](https://salu133445.github.io/bach-violin-dataset/) for the violin and [MAESTRO Dataset](https://magenta.tensorflow.org/datasets/maestro) for the piano.

The Bach Violin Dataset is a collection of high-quality public recordings of Bach’s sonatas and partitas for solo violin (BWV 1001–1006). The dataset consists of 6.5 hours of professional recordings from 17 violinists recorded in various recording setups. It also provides the reference scores and estimated alignments between the recordings and scores. The dataset and the source code for the alignment process can be found [here](https://salu133445.github.io/bach-violin-dataset/).

## Audio samples

Audio samples synthesized by our proposed model can be found in the `samples` directory and on our project [homepage](https://salu133445.github.io/deepperformer).

## Paper

__Deep Performer: Score-to-Audio Music Performance Synthesis__<br>
Hao-Wen Dong, Cong Zhou, Taylor Berg-Kirkpatrick, and Julian McAuley<br>
_Proceedings of the IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)_, 2022<br>
[[homepage](https://github.com/salu133445/deepperformer)] [[reviews](https://github.com/salu133445/deepperformer/pdf/deepperformer-icassp2022-reviews.pdf)]
