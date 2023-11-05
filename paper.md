# Abstract

Probably leave this for last.



# Introduction

Assigned this to Nema.



# Summary of symposium and large group discussions

TODO



# Final day: think tanks for specific issues

## Infrastructure, formats, and standardization of data on the DANDI archive

- summarize the technical discussion from the third day; assign Yarik, Oliver, and perhaps Horea?
- emphasize why rigorous data formats like NWB are necessary for an efficient archive and why a persistent docustore representation is easier to maintain than a live database (since we get this question a fair amount by experimental groups both large and small)

One thing I would mention here is the internal discussions we've always had that there's no such thing as files or databases - everything is just a way of organizing bytes. We can even talk about standardizing in-memory representations from arbitrary (since that is required for writing to NWB anyway) but that gives an opportunity to discuss how much more inefficient it would be from an archive perspective. We're also currently writing a NeuroConv/GUIDE paper on the challenges of supporting read from 40+ different file formats so there's a little interplay there.


## Applying deep computations to the DANDI archive

- Dendro service as for 'how'
- We certainly _can_ run whatever methods we want over all the assets on the archive that possess the correct data types for the method, but people have concerns that irregularities and lack of metadata could be an issue
- advocating for greater rigor in metadata annotation to make
- subject sneezing (not annotated and no video), train occurring on regular schedule (also not annotated), naturally occurring seizure in IBL data session (also not annotated); people worry such artifacts could be identified and misinterpreted


## Harnessing large language models (LLMs) to improve the user experience

- current advances across the field (OntoGPT, CN onto recommender service)
- search app (Luiz or Jais? have they merged?)
- LLMs that can 'summarize' contents of publication to help answer
- roadmap of where we would like LLMs to go in the long term


## Leveraging the DANDI archive for education of neuroscience

- Assign Ben, Coleen, and Jerome?
- Allen handbook
- Example notebooks
- Greatist hits
- Something like https://rosalind.info/problems/locations/ but for neurophysiology, and uses DANDI assets

