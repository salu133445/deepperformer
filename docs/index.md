Deep Performer is a novel three-stage system for score-to-audio music performance synthesis. It is based on a transformer encoder-decoder architecture commonly used in text-to-speech synthesis. In order to handle polyphonic music inputs, we propose a new _polyphonic mixer_ for aligning the encoder and decoder. Moreover, we propose a new _note-wise positional encoding_ for providing a fine-grained conditioning to the model so that the model can learn to behave differently at the beginning, middle and end of a note.

![deepperformer](assets/images/deepperformer.jpg)

Here are some audio samples synthesized by our proposed system.

| Violin | Piano |
|:-:|:-:|
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1002_mov2_009.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R1_2011_MID--AUDIO_R1-D2_09_Track09_wav_003.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1003_mov2_004.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_05_R2_2006_01_ORIG_MID--AUDIO_05_R2_2006_01_Track01_wav_146.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_emil-telmanyi_bwv1006_mov1_033.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_06_R2_2008_01-05_ORIG_MID--AUDIO_06_R2_2008_wav--3_025.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_karen-gomyo_bwv1006_mov4_012.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_MIDI-Unprocessed_14_R1_2009_06-08_ORIG_MID--AUDIO_14_R1_2009_14_R1_2009_08_WAV_120.wav" %} |
| {% include audio_player.html filename="violin/fastspeech-full/fastspeech-full_oliver-colbentson_bwv1006_mov7_006.wav" %} | {% include audio_player.html filename="piano/fastspeech-full/fastspeech-full_ORIG-MIDI_01_7_6_13_Group__MID--AUDIO_04_R1_2013_wav--4_035.wav" %} |
