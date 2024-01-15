**Guiding principles**

- try to be as concise as possible with this paper; a lot happened and it would take a lot of text space to describe everything in detail
- a big point to the release of this paper is the transparency it will afford to what was otherwise a fairly tight-knit conference that will no doubt receive ongoing attention from the community (based on how quickly the signups for the event filled up)
- up until the technical discussions of the third day, attempt to minimize specific references to the DANDI archive; it is no secret that the DANDI team organized the conference, and slight preference was given to selecting speakers that have high-profile dandisets, but the conference itself was not intended as a direct advertisement of the archive; rather it indirectly showed all the great science that could be enabled if open data sharing as a guiding principle was more prominent in our field
- the technical discussions from the last day inevitably became questions of how to make the archive better, so making that the focus of the last section is fine; also using this as an opportunity to publicize the DANDI roadmap a bit more explicitly would be great



# Abstract

Probably leave this for last, if we need it.



# Introduction



# Summary of symposium and large group discussions

[goal with this section is to keep each summary limited to 3-5 sentences; very concise with focus on the most novel aspects]

All talks and ensuing discussions were recorded live and released publicly on the DANDI youtube page (https://www.youtube.com/@dandiarchive/playlists).


1.1 New devices and high throughput acquisitions

[...]

[The most important thing to note here is the FAQ of ‘can DANDI handle all the raw data’ + ‘what about PB scale data’? + Satras answer of ‘until we generate 25+ PB a year, like CERN, we won’t have to think about storing only processed data’]

1.2 Neuroinformatics of Neurophysiologyneurophysiology

[...]

1.3 Platforms/Infrastructures

[...]

2.1 “OpenData2Knowledge”

[...]

2.2 Neuroscience Toolkits

[...]

[most important thing to note here was ecephys conversation about how no agreement in community as to if truly accurate spike sorting matters (dimensionality reduction washes it out anyway?), relative to conversation of whether we actually need to keep raw data around after collecting it]

2.3 Modeling and benchmarking

[...]



# Breakout Session - Infrastructure, formats, and standardization of data on the DANDI archive

- assigned primarily to Ryan Ly

- summarize the technical discussion from the third day; assign Yarik, Oliver, and perhaps Horea?
- emphasize why rigorous data formats like NWB are necessary for an efficient archive and why a persistent docustore representation is easier to maintain than a live database (since we get this question a fair amount by experimental groups both large and small)

One thing I would mention here is the internal discussions we've always had that there's no such thing as files or databases - everything is just a way of organizing bytes. We can even talk about standardizing in-memory representations from arbitrary source data formats (since that is required for writing to NWB anyway) but that gives an opportunity to discuss how much more inefficient it would be from an archive perspective.



# Breakout Session - AI/ML, ​​computing & visualization




# Looking forward

## Harnessing large language models (LLMs) to improve the user experience

- current advances across the field (OntoGPT, CN onto recommender service)
- search app (Luiz or Jais? have they merged?)
- LLMs that can 'summarize' contents of publication to help answer
- roadmap of where we would like LLMs to go in the long term


## Leveraging the DANDI archive for education of neuroscience

- Assign Ben, Coleen, and Jerome?
- Allen handbook
- Example notebooks
- 'Greatist hits'
- Something like https://rosalind.info/problems/locations/ but for neurophysiology, and uses DANDI assets

