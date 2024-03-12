# Abstract

Probably leave this for last, if we need it.



# Introduction

The symposium for Open Data in Neuroscience (ODIN) 2023 was the first meeting organized by the initiative of the same name from the McGovern Institute for Brain Research at the Massachusetts Institute of Technology. The gathering sought to bring together scientists at the forefront of developing state-of-the-art tools, methods, and models for neurophysiology data. Special attention was given to recent and in-progress advances in anticipation of what these technologies would be capable of achieving in the coming years, with a strong emphasis on what challenges they might pose to current data infrastructure (both storage and computation), as well as a solicitation of ideas and discussion for alleviating such challenges.

The format of the meeting consisted of rounds of lightning presentations (10-15 minute maximum) organized by topic, similar to the style of Brain Initiative meetings and short talks at COSYNE. These topics spanned acquisition devices, informatics, processing methods, and simulated models of neural activity. Highlighted throughout were recent large scale open releases of neurodata, as well as new insights that have been gleaned from previously released datasets. Presenters were chosen by the organizing board from a competitive pool of scientists representing a diverse range of subfields of neurophysiology; the presenters spanned a range of early career to veteran members of the community.

Each round of talks was followed by an interactive discussion between the audience and presenters. Each day was additionally followed by a group discussion which focused on common themes linking that day's topics.

In the final day of the meeting, the audience and presenters broke into small discussion groups tasked with delving in greater detail into the problems faced by neurophysiology as a field, and proposed solutions.

In this paper, we have compiled brief summaries of each round of talks (the full versions of which have been freely posted online for public viewing), as well as syntheses of the breakout sessions on the final day, which have not previously been made publicly available.



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

There was a growing sentiment throughout the main symposium that there is already no shortage of machine learning models waiting to be used to meta-analyze the contents of NIH open data repositories such as DANDI. Instead, the quality of data annotation by data submitters was brought into question: in practice, will the data standards enforced by these repositories require enough provenance informance and detail to properly describe the parameters of a session? [I don't think workflow is the right term here - how about parameters?]

The creation and maintenance of what have historically been considered strong training datasets for machine learning, such as MNIST [10.1109/MSP.2012.2211477] in computer vision or GigaSpeech [
https://doi.org/10.48550/arXiv.2106.06909] for speech recognition, requires a non-trivial effort by the maintainers to minimize the inclusion of incorrectly labeled samples. Of course, the sheer simplicity and homogeneity of data types in these classic examples contributes to their high reusability, in contrast to data from neurophysiology experiments which are often designed specifically to answer an experimenter's particular question of interest. Thankfully, there are common data elements within specific modalities, such as fluorescence traces extracted from optical regions of interest, spike trains sorted from extracellular probes or an animal's running velocity on a disk. Other context-dependent data streams such as estimated pose, sensory stimuli, trial structure, optogenetic stimulation, _etc._ may fall into specific categories that share commonalities such as open field exploration vs. maze navigation or static vs. drifting visual gratings. However, more specific descriptors are typically needed to fully capture the unique features of these data streams. Annotating behavioral aspects of the experiment in particular is often the hardest part of standardization, and it is the hope that larger-scale efforts such as BEADL [https://doi.org/10.1101/2024.01.08.574597] or HED [https://doi.org/10.3389/fninf.2016.00042] will offer a path towards improving behavioural data annotations, thus enhancing reusability.

There are two major cases of reproducibility raised by participants using recent examples from their own experience.

The first is recording enough of the hyperparameters and metadata, including software versions, used in complex calculations such as spike sorting to allow anyone else to generate identical results on the same raw data. As per the discussion following the Neuropixels presentation at the main symposium, there is no agreement within the community as to whether this type of fine-grain reproducibility is entirely necessary for scientific purposes.

The second case is adequate documentation of anomalies that occurred during a session which were not an intentional aspect of the task protocol and had no temporal synchronization in place to accurately demarcate the relative timing of the vent on neural timescales. Examples given of this include a naturally occurring seizure [cite session of IBL], sneezing, and significant disruptions to the building the experiment is being performed within, such as earthquakes or passing trains. On most occasions, the experimentalists reporting these events admitted they did not even record these events using handwritten notes. In some cases, there may have been synchronized video streams of the subject which could be used to estimate anomaly intervals after the fact, but some task protocols did not allow for even this. The concern of participants of this discussion was that machine learning methods, without adequate capability of filtering such events, may either spuriously flag them of items of interest or if used in training in the algorithms could introduce unintended biases when applied to non-anomalous data.

To aid reusers of data on neurophysiology archives, it was proposed in our discussion that archives should provide a set of summary quality metrics. Such metrics could also be provided as a common software package for experimentalists to use in real-time as they collect the data, or even in their decision to use the data in their own analyses, and finally whether or not to contribute it forward to a common archive. Past examples of success for this approach is the **MRIQC** package for MRI neuroimaging [https://doi.org/10.1371/journal.pone.0184661]. Nearly all of the modalities mentioned so far have at least a few agreed-upon metrics of data quality that could be calculated on archive data and reported back to allow differentiation between datasets or even selectivity of sessions within a dataset.


## Temporal alignment of neural and behavioral streams

The typical structure of neurophysiology experiments involves simultaneous acquisition from neural recordings and behavioral tracking. Given the fast timescales of neural activity, it is extremely important to have precise synchronization between these data streams. Over time, individual labs have either had to develop in-house rigs, adjusting these on a per-experiment basis, or otherwise purchase pre-fabricated setups offered by select manufacturers. The latter can be very expensive - as well as induce vendor lock-in for both systems, which can make adding additional streams even more difficult - and the former introduces additional complexity that must be considered in the design of the experiment [this statement is vague to me: what did you have in mind?] [Also, do we want to mention the risk of error that comes in-house rigs?]. This complexity is raised by this discussion group as one of the predominant challenges for good experimental design in our field of neuroscience. Exacerbating this challenge is a lack of educational resources and common 'how to' guides that could help students and newly started labs reduce the barrier of entry. [We might also want to mention the problem of high turnover and thus lack of knowledge transfer.]

We propose that a possible solution to alleviate these issues could be the creation of a repository designated purely for publically documenting experimental protocols. As it currently stands, most methods and supplemental sections of publications do not go into sufficient depth when it comes to low-level details, like implementing temporal alignment. So if a researcher wanted to reproduce or extend a design used in a publication, they would almost certainly have to reach out to the authors to discover specific details - a process that has a perceptively high energy barrier for both sides involved. It is believed that contributing these detailed instructions in a standardized and validated way could not only improve communication between labs, but also lead to overall better designs, and reduce the time it takes to design future experiments. Importantly, the goal of such an approach would not be to stifle creativity in experimental designs, but rather to provide a common location in which the community can participate in the exchange of ideas.

Yet, the argument can be made that there is inherent pragmatic value in having students and postdocs learn the details of designing an entire neurophysiology experiment. This can reduce the risk of the experimenter not understanding the low-level design details of a rig that was either pre-fabricated or inherited from prior generations in the lab. This lack of understanding could otherwise introduce artifacts and usage errors leading to spurious scientific conclusions.


### Vocabulary of neural patterns

While there has been some progress towards standardizing representations of behavior, there is less agreement concerning the characterization of repeated micropatterns of neural activity. This includes classifying cell type from the waveform of a unit during a spiking event or identifying types of ripple activity observed over time or in response to stimuli. In many cases, neural activity is labeled using the human eye and expert judgment, in conjunction with knowledge of behavioral information that may not be readily determined by looking at raw data alone, like the task the subject was performing and the state of consciousness they were in. These classifications and labels are then relied on to address specific scientific questions. Participants in this symposium believe this may not be a sufficiently rigorous method of describing patterns of neural activity and recommend further efforts in standardizing both definitions and labeling pipelines [I added "labeling pipelines" because I wasn't seeing the link with the reliance on behavioral information, but perhaps I've changed the meaning of this paragraph too much]. The neural avalanche (defined as "a sequence of consecutively active frames that was preceded by a blank frame and ended with a blank frame", using a 'reasonable' choice of $\Delta t$ time window [10.1523/JNEUROSCI.23-35-11167.2003]) is a good example of such a pattern that is quantifiable based on common criteria agreed upon by a community of researchers.

These differences in human codification, even among experts, are not unique to neurophysiology - [Catherine’s example of human consensus among pathologists which was highly variant. I think there was another case we can cite with climate science?]. In some cases, such as experimentally induced stimulation [<= I think this may be too vague, as I'm what types of datasets this phrase is meant to include or exclude], one way to improve specificity and consistency in data labeling could be to allocate some portions of public datasets to be hidden from direct access, but usable for serverside verification: a common approach for testing machine learning methods, especially in competition frameworks.

Here, we have a dilemma: researchers must make assumptions relevant to their hypothesis of interest to reach local conclusions in the context of their study [<= I think there is a missing point here, which is that these assumptions shape their data curation, and therefore other people's ability to reuse their dataset for different question]. However, the wider scientific community could benefit significantly from datasets being labeled using common precisely defined metrics. Thankfully, funding agencies such as the NIH have been aware of this shortcoming of neuroscience for some time, going so far as to launch a new initiative for Brabin Behavior Quantification Synchronization (BBQS) [how to cite?] to seek answers to such questions. [<= I would make this sentence more neutral]



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

