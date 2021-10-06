# DeepPerformer: Score-to-audio music performance synthesis

DeepPerformer is a novel three-stage system for score-to-audio music performance synthesis. It is based on a transformer encoder-decoder architecture commonly used in text-to-speech synthesis. In order to handle polyphonic music inputs, we propose a new _polyphonic mixer_ for aligning the encoder and decoder. Moreover, we propose a new _note-wise positional encoding_ for providing a fine-grained conditioning to the model.

## Dataset

The Bach Violin Dataset is available [here](https://salu133445.github.io/bach-violin/).

## Audio samples

Examples of audio files synthesized by our proposed model can be found [here](https://salu133445.github.io/deepperformer). Audio samples used in the subjective listening test can be found [here](https://salu133445.github.io/deepperformer/violin) (violin) and [here](https://salu133445.github.io/deepperformer/piano) (piano).
