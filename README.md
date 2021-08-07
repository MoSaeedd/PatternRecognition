# PatternRecognition

The project task is about the development of a pattern recognizer for the classification of different environments on the basis of audio files. For this purpose, data were recorded from different environments in different cities. Altogether the four cases airport, bus, metro station and public square should be differentiated.

Each audio file has been converted into features. The audio data was originally recorded at 48 kHz on a portable recorder and had a duration of 10 seconds. In a second step, the data recorded in this way were broken down into 64 frequency bands with the aid of a Gammaton filter bank. The lowest band is at a frequency of 50 Hz, while the highest band is at 24 kHz.
The arrangement of the so-called Gammaton filters was determined equidistantly on the ERB scale (Equivalent Rectangular Bandwidth). According to this model, more bands are used for low frequencies than for high frequencies, which corresponds to the properties of the human hearing.
The Gammaton spectra were calculated on 25 ms long windows, each of which was advanced by 10 ms over the audio signal x (t), so that a 10 second long signal resulted in a total of 998 values for each band. Then we used the magnitude and a nonlinear transformation for each band in order to make the resulting so-called gammatongram X ∈ R64 × 998 clearer. The features generated in X are accordingly a time-frequency representation.
I used a CNN classifier over the histogram to make use of the temporal sequnce of sounds (CNN works well for the purpose). 

##Procedure
First, many simple classifiers were tested alongside with dimensionality reduction techniques (LDA and PCA). The maximum testing accuracy was around 80%.
We have then used a CNN with feature normalization and managed to get 94% accuracy on test dataset.
We have used keras with TF.

## Results
This was part of a competetion and we achieved 1st place with 77% accuracy on totally different dataset



