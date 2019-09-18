# Million Song Dataset - Additions and Benchmarks

## Overview

The [Million Song Dataset (MSD)](http://labrosa.ee.columbia.edu/millionsong/) [[1\]](http://www.ifs.tuwien.ac.at/mir/msd/#refs1), a collection of one million western popular music pieces, has enabled a large-scale research for many MIR applications. The dataset comes with a set of features extracted by the former API of [The Echonest](http://echonest.com), which include tempo, loudness, timings of fade-in and fade-out, and MFCC-like features for a number of segments.       

The dataset does however not provide an easy download possibility for the audio files, thus researchers are basically limited to the features provided with the dataset. Using a content provider, for which links with unique IDs to the internal database existed in the MSD, we downloaded [audio samples](http://www.ifs.tuwien.ac.at/mir/msd/collectionCharacteristics.html), mostly in the form of 30 or 60 second snippets. Subsequently, we provide a [multitude of features](http://www.ifs.tuwien.ac.at/mir/msd/download.html) extracted from these samples, to allow comparison between them.       

## Contributors

- Alexander Schindler
- Rudolf Mayer
- Thomas Lidy
- Peter Knees
- Andreas Rauber

## Ground Truth Assignments

To allow for popular tasks in Music Information retrieval research such as musical genre classification, we  further provide a [categorisation](http://www.ifs.tuwien.ac.at/mir/msd/download.html#groundtruth) of a subset of the collection into genres obtained from the All Music Guide ([allmusic.com](http://allmusic.com)). 

AllMusic is a Web portal of a large music information database including album reviews, artist biographies as well as expert tagging for albums according into genres, styles, moods and themes. Data-collection is aligned to \cite{schindler2012}. Meta-data was automatically collected from AllMusic using a web-scraping script based on direct string matching to query for artist-release combinations. From the resulting Album Web page genre, style, mood and theme tags were collected (see Table \ref{tab:tags_overview}). 

### Genres

The *Genres Tag-Set* is the largest collection with a skewed distribution towards the label 'Pop/Rock'. The set further contains cross-genre tags such as *Holiday* and *Children*.

### Styles

The *Styles Tag-Set* complement genres and provide a more detailed description of music characteristic such as rhythm, harmony, instrumentation, etc. 

### Moods

Tags of the *Moods Tag-Set* depict emotions expressed by the music.

### Themes

The *Themes Tag-Set* describes certain cross-genre scenarios or occasions such as holiday, party or Christmas.


We further provide a number of [splits into training / test sets](http://www.ifs.tuwien.ac.at/mir/msd/download.html#splits) that should ensure comparability of the experiments. These are in detail: 

- "Traditional" split with 2/3 training and 1/3 testing data
- Split with a large proportion of training data
- Split with a small proportion of training data



# Papers / Studies

- Alexander Schindler and Peter Knees. Multi-Task Music Representation Learning from Multi-Label Embeddings. In Proceedings of the International Conference on Content-Based Multimedia Indexing (CBMI2019). Dublin, Ireland, 4-6 Sept 2019.
- Alexander Schindler, Thomas Lidy, and Andreas Rauber. Comparing shallow versus deep neural network architectures for automatic music genre classification. In Proceedings of the 9th Forum Media Technology (FMT2016), St. Poelten, Austria, November 23 - November 24 2016. 
- Alexander Schindler and Andreas Rauber. Capturing the temporal domain in echonest features for improved classification effectiveness. In Adaptive Multimedia Retrieval, Lecture Notes in Computer Science, Copenhagen, Denmark, October 24-25 2012. Springer.
- Alexander Schindler, Rudolf Mayer, and Andreas Rauber. Facilitating comprehensive benchmarking experiments on the million song dataset. In Proceedings of the 13th International Society for Music Information Retrieval Conference (ISMIR 2012), pages 469-474, Porto, Portugal, October 8-12 2012.
- Alexander Schindler. Million song dataset integration into the clubmixer framework. In Proceedings of the 12th International Society for Music Information Retrieval Conference (ISMIR 2011), Miami, USA, October 24-28 2011.