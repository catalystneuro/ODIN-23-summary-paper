# Abstract

Probably leave this for last, if we need it.



# Introduction



# Summary of symposium and large group discussions

[goal with this section is to keep each summary limited to 3-5 sentences; very concise with focus on the most novel aspects]

All talks and ensuing discussions were recorded live and released publicly on the DANDI youtube page (https://www.youtube.com/@dandiarchive/playlists).

[Question: What do we want to do in terms of speaker names and bibliographical references? I've referenced when it seemed applicable, but mostly refer to project names and not the authors/creators.]

1.1 New devices and high throughput acquisitions

When selecting brain recording technologies to use in their studies, researchers generally must make a compromise between optimizing temporal resolution, spatial resolution and brain coverage. Fortunately, new technologies continue to push the boundaries of this trade-off, improving the combined resolution and coverage that can be achieved using a single recording modality. These include Neuropixels, a silicon probe which allows high-density simultaneous recording of hundreds of neurons in awake and freely moving animals {cite}`Jun2017`. More recently, thin-film, multithousand-channel recording grids using platinum nanorods (PtNRGrids) have been developed which enable highly dense recordings of brain surface activity in human patients, allowing researchers to resolve the dynamics of normal and pathological activity at high spatial and temporal resolutions {cite}`Tchoe2022`. In the field of two-photon imaging, light beads microscopy now enables volumetric recordings of single cell activity across the entire cortex {cite}`Demas2021`. At the circuit level, improvements in voltage imaging now allow researchers to optically resolve sub-threshold activity across the dendritic tree of single cells {cite}`Adam2019`.

Technological advances such as these are poised to revolutionize the quantity and quality of data available to the neuroscience community. However, the high-throughput of these devices in turn raises an important concern for open science: Will neurophysiological data repositories be able to handle the TBs of data generated, or will we have to move to storing only pre-processed data? For large-scale repositories like DANDI, the answer is that until we begin to generate 25+ PB a year, like the European Organization for Nuclear Research (CERN) does, there is sufficient capacity to store and share this data.

1.2 Neuroinformatics of Neurophysiology
 
Numerous new tools have emerged in the last decade to address the needs of the open science community when it comes to creating and sharing open datasets, as well as interacting with them. These include the Neurophysiology Without Borders (NWB) format, which aims to be a flexible and accessible standard for sharing neurophysiology data between research laboratories {cite}`Rubel2022`. Since its introduction, new tools like NeuroConv and NWB GUIDE have been developed to make converting proprietary data to the NWB format more intuitive for researchers aiming to share their data. Developed hand-in-hand with the NWB data standard, the DANDI repository (Distributed Archives for Neurophysiology Data Integration) provides an open access option for sharing neurophysiology data broadly, accepting raw and  processed electrophysiology and optophysiology standardized data from any species {cite}`Rubel2022`. As mentioned above, the DANDI repository is growing quickly, comprising already 200 TB of neurophysiology data at the time of this meeting, and is poised to welcome much more data over the coming years.

The large amounts of data being collected and their growing complexity also place high demands on research laboratories, increasing the technological skills required to collect, manage and analyse this data. Efficient, scalable and reproducible research tools are needed to support researchers in collecting high-quality datasets and performing reliable analyses. To this end, new commercial services are emerging, like DataJoint, which helps laboratories design and scale end-to-end data collection, analysis and sharing pipelines {cite}`Yatsenko2018`, and CatalystNeuro which works with neuroscientists to provide customized software solutions to their specific needs. Finally, open web-based tools are also being developed to allow researchers to interact with and visualize the increasingly accessible, complex and plentiful data available online. Neurosift allows users to visualize data recorded in NWB files hosted in the cloud, without having to download large datasets locally, while Dendro is currently being developed as a web app for analyzing data stored in the cloud or locally. As figures in research papers become increasingly complex and multi-dimensional, Figurl provides a framework for creating and sharing interactive visualizations of data and data analysis results. 

Looking forward, it is clear that tools such as these are critical for ensuring that researchers can keep up with the quantity and complexity of neurophysiology data being generated. It is agreed, however, that the usability of these tools and the availability of user support resources are critical for their wide-spread adoption. The barrier to entry must be kept low to ensure that researchers can efficiently and effectively integrate these new tools into their workflows. 


1.3 Platforms/Infrastructures

As the complexity, operational cost and scale of new neurophysiology technologies has increased, so has the challenge of ensuring the importance of developing large-scale collaborative projects, going beyond the traditional single laboratory model. Such projects allow large groups of researchers with wide-ranging expertise and access to cutting-edge technologies to collaborate on the creation of high quality datasets for the community at large to use. For example, Japanese Brain/MINDS brain-mapping project enabling the creation of a comprehensive and integrated database of marmoset brains {cite}`Okano2015;Woodward2018;Hata2023;Skibbe2023`. The Allen Institute for Neural Dynamics has been working on collecting large-scale neural circuit mapping data in mice, to add to the Allen Institute's openly shared datasets. To support open, reproducible, and versioned analysis and processing, they aim to deploy public analysis pipelines, alongside their datasets, using tools like Code Ocean, which provides an interactive interface for scientists to explore and analyse datasets without having to develop all the skills of a software engineer.

Also leveraging the Allen Institute's extensive resource, the OpenScope initiative was created to support researchers who have ideas for valuable datasets, but lack the necessary resources to collect them in their own laboratories. Experimental proposals from external scientists are selected yearly for their feasibility and scientific merit, and deployed in close collaboration, using the Allen Brain Observatory pipeline. After an initial period during which the proposing team has priority access, the datasets are published for open access use by the neuroscience community at large. The International Brain Laboratory (IBL), for its part, provides a decentralized model for ensuring the reproducibility and reliability of neuroscience data and research. For its first project, the IBL, comprising researchers from 22 laboratories in 6 countries, collaborated on designing a standardized experiment for probing the role of neural circuits in decision-making. Once the experiment, standardized from data collection to analysis, had been carried out in each laboratory, the findings and data were jointly published, to ensure maximal reproducibility and reliability of the findings {cite}`International2021;International2023`. As of neuroscience research matures and projects increase in scope and complexity,
initiatives like these, which connect traditional academic research laboratories around the world and generate foundational databases for the field, will become increasingly important.

2.1 “OpenData2Knowledge”

[...]

2.2 Neuroscience Toolkits

[Dr. Mathis's talk on CEBRA here]

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

