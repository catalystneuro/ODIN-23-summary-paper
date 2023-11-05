**Guiding principles**

- try to be as concise as possible with this paper; a lot happened and it would take a lot of text space to describe everything in detail
- a big point to the release of this paper is the transparency it will afford to what was otherwise a fairly tight-knit conference that will no doubt receive ongoing attention from the community (based on how quickly the signups for the event filled up)
- up until the technical discussions of the third day, attempt to minimize specific references to the DANDI archive; it is no secret that the DANDI team organized the conference, and slight preference was given to selecting speakers that have high-profile dandisets, but the conference itself was not intended as a direct advertisement of the archive; rather it indirectly showed all the great science that could be enabled if open data sharing as a guiding principle was more prominent in our field
- the technical discussions from the last day inevitably became questions of how to make the archive better, so making that the focus of the last section is fine; also using this as an opportunity to publicize the DANDI roadmap a bit more explicitly would be great



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

