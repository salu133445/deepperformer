# Dataset

We used two datasets to train our proposed system: [Bach Violin Dataset](https://salu133445.github.io/bach-violin-dataset/) for the violin and [MAESTRO Dataset](https://magenta.tensorflow.org/datasets/maestro) for the piano.

The Bach Violin Dataset is a collection of high-quality public recordings of Bach’s sonatas and partitas for solo violin (BWV 1001–1006). The dataset consists of 6.5 hours of professional recordings from 17 violinists recorded in various recording setups. It also provides the reference scores and estimated alignments between the recordings and scores. Below is an example of the alignment provided, where white dots and green lines show the estimated note onsets and durations.

![alignment](assets/images/alignment.jpg){: style="max-height: 200px; width: 600px; max-width: 100%;"}

{% include audio_player.html filename="assets/audio/emil-telmanyi_bwv1001_trimmed_30sec.mp3" %}

_For more information, please visit our project [homepage](https://salu133445.github.io/bach-violin-dataset/)._
