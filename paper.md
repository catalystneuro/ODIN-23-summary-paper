# Abstract

Probably leave this for last, if we need it.



# Introduction

The symposium for Open Data in Neuroscience (ODIN) 2023 was the first meeting organized by the initiative of the same name by the McGovern Institute for Brain Research at the Massachusetts Institute of Technology. The gathering sought to bring together scientists at the forefront of developing state-of-the-art tools, methods, and models of neurophysiology data. Special attention was given to recent and in-progress advances in anticipation of what these technologies would be capable of achieving in the coming years, with a strong emphasis on what the challenges they might pose to current data infrastructure (both storage and computation) as well as solicitation of ideas and discussion for alleviating such challenges.

The format of the meeting followed rounds of lightning presentations (10-15 minute maximum) within a related topic, similar to the style of Brain Initiative meetings and short talks at COSYNE. These topics spanned acquisition devices, informatics, processing methods, and simulated models of neural activity. Highlighted throughout was recent large scale open releases of neurodata, as well as new insights that have been gleaned from previously released datasets. Presenters were chosen by the organizing board from a competitive pool of scientists across the a diverse representation of subfields of neurophysiology; the presenters spanned a range of early career to veteran members of the community.

Each round of talks was followed by an interactive discussion between the audience and presenters. Each day was additionally followed by a group discussion which brought together a focus on common themes spanned by that days topics.

In the final day of the meeting, the audience and presenters broke into small discussion groups tasked with delving into greater detail the problems and proposed solutions faced by neurophysiology as a field.

In this paper, we have compiled some brief summaries of each round of talks (the full versions of which have been freely posted online for public viewing), as well as the recorded details of the breakout sessions of the final day, which have not previously been made publicly available.



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

