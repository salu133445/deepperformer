# Deep Performer: Score-to-audio music performance synthesis

Deep Performer is a novel three-stage system for score-to-audio music performance synthesis. It is based on a transformer encoder-decoder architecture commonly used in text-to-speech synthesis. In order to handle polyphonic music inputs, we propose a new _polyphonic mixer_ for aligning the encoder and decoder. Moreover, we propose a new _note-wise positional encoding_ for providing a fine-grained conditioning to the model so that the model can learn to behave differently at the beginning, middle and end of a note.

## Dataset

To train our proposed system, we compile a new dataset of 6.5 hours of professional violin recordings along with their scores and estimated alignments. The dataset and the source code for the alignment process can be found [here](https://salu133445.github.io/bach-violin-dataset/).

## Audio samples

Examples of audio files synthesized by our proposed model can be found [here](https://salu133445.github.io/deepperformer). Audio samples used in the subjective listening test can be found [here](https://salu133445.github.io/deepperformer/violin) (violin) and [here](https://salu133445.github.io/deepperformer/piano) (piano).

## Paper

__Deep Performer: Score-to-Audio Music Performance Synthesis__<br>
Hao-Wen Dong, Cong Zhou, Taylor Berg-Kirkpatrick, and Julian McAuley<br>
_Proceedings of the IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)_, 2022<br>
[[homepage](https://github.com/salu133445/deepperformer)]
