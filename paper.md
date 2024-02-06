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

This discussion identified three main problems curbing the full potential of modern statistical learning methods applied to open neurophysiology datasets, including limits on the universality of computations or processing algorithms, as well as side-effects that can limit the application of even simple visualization software. The most immediate challenge is the vast diversity and heterogeneity of neurophysiology experiments, and how to ensure the overall level of quality for metaanalysis capability; referred to as an ‘AI-ready dataset’. Also noted is the increasingly complex challenge of achieving precise temporal synchronization across a number of acquisition devices so be able to associate exact event timing from behavior to those of the neural streams; a practice used in nearly every modern experiment on live subjects, yet one that is still done ad hoc by individuals labs. Finally, echoing the voices of the main symposium, the lack of community agreement for a common vocabulary of neural patterns hampers the ability for statistical learning approaches to generalize beyond the context window of a single experiment archetype.

The group also noted that communication on the low-level details of these topics is exceptionally difficult as different labs across the country, and across the world, have developed their own language for referring to certain concepts and approaches of task protocol design and development of experimental rigs - pointing to a need for tighter community interactions, or at least more common and frequent grounds for conversing across groups.


## Consistent curation of diverse data

There was a growing sentiment throughout the main symposium that there is no current shortage of machine learning models awaiting to be used to meta-analyze the contents of NIH open data archives such as DANDI. Instead, there was question of the quality of data annotation by experimentalists; in practice, will the data standards used by these archives require enough provenance and detail in describing the workflow of a session?

The creation and maintenance of what are historically considered strong AI-ready training datasets, such as MNIST [cite], [add audio], or most others linked on [add generic compilation?].

[homogeneity of data compared to other standard ML training sets in audio/vision/text/etc]

[experimentalists would greatly appreciate quality metrics for a given experiment to be returned immediately after or even during in real time; lack of agreed upon universal metrics for all modalities, but some exist for ecephys and ophys raw data quality ; QC could eventually adapt to detect anomalous events]

[cite MRIQC software for quality metrics]

[ability to directly compare quality metrics of two similar NWB files]

There are two major cases of reproducibility raised by participants using recent examples from their own experience.

The first is recording enough of the hyperparameters and metadata, including software versions, used in complex calculations such as spike sorting to allow anyone else to generate identical results on the same raw data. As per the discussion following the Neuropixels presentation at the main symposium, there is no agreement within the community as to if this type of fine-grain reproducibility is entirely necessary for scientific purposes.

The second case is adequate documentation of anomalies that occurred during the course of a session which were not an intentional aspect of the task protocol and had no temporal synchronization in place to accurately demarcate the relative timing of the vent on neural timescales. Examples given of this include a naturally occurring seizure [cite session of IBL], sneezing, and significant disruptions to the building the experiment is being performed within, such as earthquakes or passing trains. On most occasions, the experimentalists reporting these events admitted they did not even record these events using hand written notes. In some cases there may have been synchronized video streams of the subject which could be used to estimate anomaly intervals after the fact, but some task protocols did not allow for even this. The concern by participants of this discussion was that machine learning methods, without adequate capability of filtering such events, may either spuriously flag them of items of interest, or if used in training in the algorithms could introduce unintended biases when applied to non-anomalous data.

[wider use of HED]


## Temporal alignment of neural and behavioral streams

[Difficulty of temporal alignment in task protocols and lack of standard supported approaches (labs usually have to rig them entirely themselves ad hoc) - connects to bigger problem of not having a common archive of something more basic than a session of a neuroscience experiment; a standard way of describing task protocols and a common place to search for those that might be similar]

[should we mention the pragmatic value of learning to do things ourselves? Or stick to benefits of offloading the cognitive burden? Danger of generational inheritance of pre-built rigs may not understand…  Quote from discussion, “Many students hated it, many loved it and learned alot from it”]

Likewise, there were no comments by participants regarding a lack of compute resources for harnessing the information stored in these data archives, though there was noted to be an absence of educational materials for how exactly to use such resources to their full potential. This has been an ongoing effort by the open data teams, including [nimas neuromatch efforts; szonjas moser work; neurodata rehack; dandi example notebooks?]

[Can rigs and protocols be standardized without hampering creativity?]


### Vocabulary of neural patterns

[Human eye may not be best? Computer vision, cell types, other metadata]

[Catherine’s example of human consensus among pathologists which was highly variant. I think there was another case we can cite with climate science?]

[Human visualizations of information are not consistent or agreed upon - different answers among experts even on ground truth]

[Possible solution could be to codify how humans do things to inform algorithms]

[Example of sharp wave ripple definition; can even depend on knowledge of behavior task and sleep states, might not be able to tell from raw data alone]

[cite BBQS brain behavioral quantification synchronization should try to solve this problem]

[callback to HED for example of how a common language can be done in other aspects]



# Looking forward

The organizers of ODIN would like to thank all the speakers for being so concise in their presentations. They would also like to thank participants for being so active in the conference and ensuing discussions. There is a strong interest in this gathering continuing as a yearly event to facilitate open channels of communication across the diverse areas of neurophysiology and systems neuroscience.

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

