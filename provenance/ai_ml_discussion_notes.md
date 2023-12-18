These are the recorded notes from the AI/ML/Computation discussion session on the third day of ODIN 23.

# Morning

## Questions

### Do we have a consensus on what constitutes AI vs ML?

AI : a model

vs

ML : a tool to accomplish some task



### Are we moving forward something called AI? Should we call it statistical learning?

Can we use statistical learning to advance data sharing, discoveries?

Building connection between shared datasets and metadata.

Concept of NIH : AI-ready dataset

Functional genomics, voice, salutogeneis



### How to reduce complexity of data?

Brain score vision and brain score language runs on top of digital twins; can be decomposed to matrix to matrix comparison; are neural activations present at all for comparisons?

Such a high amount of diversity in data, need a common accepted standard to map things automatically to a benchmark

Fmri or eeg ; way to ensure that presenting same stimulus;  problem is temporal alignment of behavioral data to neural quantification over time

Problem is lack of standard reference experimental protocol for aligning to a common clock - so everyone does it a different ad hoc way



### Labs use a pre-configured common rig? 

Currently an extremely manual step

Cost to move away from custom 

Native, intuitive graphical interfaces alleviate 

Experimentalists had to teach themselves, no guidance, just figure it out and learn, which is valuable ; layers of abstraction to help move away from these difficulties but that can add difficulties in learning? But can also allow them to focus on a more narrow set of problems

Many students hated it, many loved it and learned alot from it

Inheritance of pre-built rigs may not understand 

Danger of trial and error is you may not even know your own mistakes until too far down teh line; story of a postdoc who lost a year of data due to bad port plug

Problem is lack of a tool that can execute neurophys experments in a standardized way that can lead to a useful format

Some rigs are sold with that, but are very expensive

Problem is a rig can have delay between raw data to key QA metrics; can be a week, but can usually be reduced to realistic timescale of the ‘same day’

Spike sorting remains a challenge; is it easier today than it was?

Lack of ability to visualize and quantify the outputs

Can use manual curation of spike sorting to obtain a consensus of automated performance

Also no agreed upon metrics for human consensus



### Can behavior on rig be standardized?

BBQS brain behavioral quantification synchronization should try to solve this problem



### Do we have the right vocabulary for talking about patterns of neural activity?

Human eye may not be best? Computer vision, cell types, other metadata

Human consensus among pathologists was highly variant

Problem: human visualizations of information are not consistent or agreed upon - different answers among experts even on ground truth

Possible solution could be to codify how humans do things to inform algorithms

Using LLMs to generate documentation 

Problem: communication on these topics is hard



## Problems

### For training trustworthy models…

temporal alignment of behavioral data to neural quantification over time

lack of standard reference experimental protocol for aligning to a common clock - so everyone does it a different ad hoc way

Lack of a tool that can execute neurophys experments in a standardized way that can lead in the end to a useful format

a rig can have delay between raw data to key QA metrics



### For benchmarking…

We don’t have a correct or agreed upon vocabulary for talking about patterns of neural activity?

Human visualizations of information are not consistent or agreed upon - different answers among experts even on ground truth





# Afternoon

## Problems

### We don’t have good metrics to create benchmarks

What quality metrics do you use?

MRIQC software is an example for compiling quality metrics



### Annotating dandiset by an external user

Somebody who did not produce the data can't easily determine some subset of channels are useless 

File connected to NWB for quality metrics

Central web server at nih storing those quality metrics

You can even compare to other NWB files to know where you are in quality

Quality metrics comes from the data themselves.

An assoicated code base to describe how it’s computed

Idea of package : neurophysQC

Bypass the human trust

For certain ripple, more controls to overcome noise

Sharp wave are more obvious, but also depends on what the animals are doing; if running, no ripple even in the right area with clean data - not easy to qualify on the data alone

**Solution: DANDIDERIVATIVES/DANDI STATS : if metrics are determined through the data, a service to compute things**



## You need to go back to the methods of the original paper to find out minor details about the dandiset.

Which part should be included in the data.

Real life example: monkey sneezed during experiment; had a huge impact to neural activity

Notes would be very hard to digitize may not be useful to anyone

Expeirmenter making files can’t predict what a re-user might want years down the road

Publishing pre-processing pipelines with a dataset

Peter Petersen Lab notebook digitalized [BrainSTEM]; NWB GUIDE Desktop application for easy metadata entry

**Solution 1: Annotations on DANDI sets would be immensely helpful**

**Solution 2: HED support to help describe rich oddities**


## Ideas

### To build a foundational model of the hippocampus. How would you integrate different models and different datasets?

**Solution 1: Integration of knowledge graph service**

Independent service from DANDI, could be helpful for publications as well**

**Solution 2: verification/approval of dandisets**

**Solution 3: more example notebooks [required? Encouraged with a star?] as a form of documentation about the dandiset**

**Solution 4: DANDI stars + leaderboard to encourage good habits**v

Constrain LLm away from bias**

**Solution 5: use LLM for keyword assignment**

**Solution 6: educational collection of ; problem of the week? With solution a week later with full explanation? Like rosalind.info [gamified]**
