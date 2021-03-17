# Barriers to reproducibility

So far we have described the [importance](../01/importantforscience) of reproducible research and motivated why we think [you should care](../02/whycare).

But there are many barriers to reproducible research.
You can watch Kirstie Whitaker describe some of them in [her talk about _The Turing Way_](https://youtu.be/wZeoZaIV0VE?t=312) at [csv,conf,v4](https://csvconf.com/2019) in May 2019.
You can use and re-use her slides under a CC-BY licence via Zenodo (doi: [10.5281/zenodo.2669547](https://doi.org/10.5281/zenodo.2669547)).
The section describing the slide below starts around 5 minutes into the video.

| ![Barriers to reproducible research](../../figures/reproducibility/barriers.png) |
| -------------------------------------------------------------------------------------------------------- |
|  Some of the barriers to reproducible research. |

This chapter outlines some of those barriers, and a couple of suggestions to get around them.

## Plead the fifth 

No-one wants to incriminate themselves, and no-one is infallible. Putting your code online can be very revealing and intimidating, and people are scared of being judged by others. However, releasing code can help other researchers provide feedback, learn and may help them in their research. Publishing your code encourages you to write your code to a high standard and can help generate new ideas. **Let the person who is without bugs report the first error.**

## Publication bias towards novel findings


Novel results are not necessarily accurate or interesting but they are rewarded in the academic world!
Papers that do not find statistically significant relationships are hard to publish, particularly if the results *do not* reproduce previously published findings.
(That includes statistically significant findings that go in the opposite direction to already published work.)
Similarly, an article might be less likely to be accepted to a journal or a confence if it successfully reproduces already-published results instead of producing a new set.
There's a good chance that reviewers will say "we already know this" and reject the submission.

John Ioannidis published an influential paper in 2005 titled "Why Most Published Research Findings Are False" (doi: [10.1371/journal.pmed.0020124](https://doi.org/10.1371/journal.pmed.0020124)) which discusses the many factors that contribute to publication bias.
Therefore it is very likely that there is a lot of duplicated work in data science.
Too many different researchers are asking the same question, not getting the answer they expect or want, and then not telling anyone what they have found.

## Held to higher standards than others

A researcher who makes their work reproducible by sharing their code and data may be held to a higher standard than other researchers.
If authors share nothing at all then all readers of a manuscript can do is trust (or not trust) the results.
If code and data are available, peer reviewers may go looking for differences in the implementation (compared to how they would have analysed the data) and require additional changes from the authors of the submitted manuscript before it is accepted for peer review.
This problem also relates to readers of a published paper scrutinising the work more carefully as described in the [Plead the Fifth](#plead-the-fifth) section above.

## Barrier 4

*replace this text with the content of barrier 4*

## Barrier 5

*replace this text with the content of barrier 5*

## Barrier 6

Takes Time

The time needed to maintain a reproducible project presents a significant barrier. At the start of the project considerable time needs to be invested in designing and setting up the reproducibility pipepine. This may include a testing framework , continuous integration, Github repository and data rights. Time may also be spent communicating with collaborators to agree which parts of the project may be open source and how they are shared, this may include creating synthetic data.Throughout the project, considerable time needs to be spent mainting the reprodicibility pipeline including refactoring, testing and resolving conflicts. At project conclusion time usually spent modifying analysis may be saved thanks to the reproducibility pipeline. However, time may be lost at review due to framework explanation and suggested adaptations.


## Barrier 7

*replace this text with the content of barrier 7*

## Big data and complex computational infrastructure

Big data is conceptualised in different ways by different researchers. 
"Big" data may be complex, come from a variety of data sources, is large in storage volume and/or be streamed at very high temporal resolution. 
Although there are ways to set random seeds and take snapshots of a dataset at a particular moment in time, it can be difficult to have identical data across different runs of an analysis pipeline.
This is particularly relevant in the context of tools for parallel computing.
For example, streaming data such as flight tracking or internet traffic can not be stored and must be processed in real time.

A more common challenge for "big data" researchers is the variability of software performance across operating systems and how quickly the tools change over time.
An almost constantly changing ecosystem of data science technologies is available, which means reproducing results in the future is highly variable and dependent on using perfectly backwards compatible tools as they develop. 
Very often the results of statistical tests will vary depending on the configuration of the infrastructure that was used in each of the experiments, making it very hard to independently reproduce a result.
Experiments are often dependent on random initialisation for iterative algorithms and not all software includes the ability to fix a pseudorandom number without limiting parallelisation capabilities (for example  e.g. in Tensorflow).
These tools can require in depth technical skills which are not widely available to data scientists.
The Hadoop framework, for instance, is extremely complex to deploy data science experiments without strong software and hardware engineering knowledge. 
Even "standard" high performance computing, can be difficult to set up to be perfectly reproducible, particularly across different cloud computing providers or institutional configurations.

## Being reproducible does not mean the answer is right

By making the code and data used to produce a result openly available to others, our results may be **reproduced** but mistakes made by the initial author can be carried through.
Getting the same wrong answer each time is a step in the right direction, but still very much a **wrong** answer!

It is important to remember that reproducibility is necessary but not sufficient for good quality research.
A critical approach is needed, rather than naively using existing software without understanding what it does.
(See, for example, [a discussion](https://ryxcommar.com/2019/08/30/scikit-learns-defaults-are-wrong) in August 2019 about whether the default settings for Scikit-learn's implementation of logistic regression are misleading to new users.)
Interperability and interoperability are required to properly evaulate the original research and to strengthen findings.
