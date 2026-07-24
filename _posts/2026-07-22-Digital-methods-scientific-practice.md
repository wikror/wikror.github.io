---
layout: post
title: "What can digital methods tell us about scientific practice?"
category: blog
keywords: digital philosophy of science, topic modeling, methodology, metaphilosophy, philosophy of science in practice, spsp
date: 2026-07-22
---

June 2026 edition of the Society for the Philosophy of Science in Practice Newsletter included my piece on the promises and limitations of digital methodology in the study of scientific practice. It is available here: [SPSP June 2026 Newsletter](https://sway.cloud.microsoft/WzkbQNheb1JEcDm6) 

I was invited Elis Jones, who guest edited the newsletter---many thanks for the amazing editorial work!

Below is the reprinted paper, with interactive visualizations:

---

Digital methods have been a major innovation in the recent history of the humanities. In
hindsight, it perhaps seems obvious that philosophers would eventually adopt these
tools and turn them back onto science itself. But it is not always so obvious exactly how
these tools might be useful for philosophers of science, particularly for those (us!)
interested in scientific *practice*.

Since around 2013, when James Overton's paper on "explanation" popularized the use
of these tools in a philosophy of science context, *digital philosophy of science* has
steadily developed as a sub-field in its own right, in part by promising to lift some of the
constraints of traditional approaches to philosophy of science. These newer approaches
still look to answer central questions of philosophy of science: for instance, how
scientific concepts develop and change, what these concepts capture, or how
researchers conceive of the aims of their research.

But digital studies can draw, at scale, on a variety of digital resources to answer those
questions: metadata and citation networks, digital databases of various disciplines, or,
most commonly, large corpora of scientific papers. Relying on computational tools of
natural language processing allows researchers to explore and map textual corpora
which extend beyond the limits of unaided cognition—what Franco Moretti called
"distant reading". Indeed, such methods can incorporate more text than can be read in a
single human lifetime. This can help extend our picture of scientific activities beyond
the (sometimes peculiar) favored case studies of our discipline. And although the
methods focus on text, they can still inform our understanding of scientific practices—or
so I would like to argue here.

Scientific publications are undeniably the primary focus of digital methods. Papers are
used to understand what role epistemic concepts like "explanation" play for researchers
(aside from the already mentioned work by Overton, more recently this question has
been studied by Christophe Malaterre and his collaborators). Digital methods can also
answer other questions, like how concepts central to different fields are defined, and
how they change meaning and gain or lose prominence (Charles Pence and Arianna
Betti focus on such historical studies, whereas in my own work I explore a more
synchronous picture).

But what are the actual practices involved in digital methods? An approach called "topic
modelling" has particular prominence. Topic modelling assumes that the "topic" to
which a given text or its part refers to can be modelled as a probability distribution over
words. "Topics" here are best understood as a specific kind of context (as philosophers
Jaimie Murdock and Colin Allen notably suggest). If we are talking about the context of
*deep learning technology*, then words like "network", "transformer", "supervised" will
have a much higher probability than in the context of, say, *geology*, where words like
"drift", "erosion", "volcanic" will be more likely.

Topic modelling algorithms, like Latent Dirichlet Allocation (LDA), attempt to infer those
probabilities from frequencies of individual words in the empirical sample, and to find
terms which differentiate documents within the sample. Words strongly and more
uniquely associated with a certain context can then be used as labels for that "topic".
This information can be used as a proxy of what the text is about. There are important
caveats though: some parameters, like the *number of "topics"*, are given by the user,
and sometimes the word groupings found via these methods do not correspond clearly
to a human-interpretable topic. In such cases interpretation proves particularly crucial—
prompting some critics to compare the process to reading from tea leaves, and more
generally—highlighting the persistence of a subjective component in these
methodologies (probably of no surprise to readers here - more on that below).

As an illustration, you can see, below, an example taken from my PhD dissertation,
where I used topic modeling to identify different contexts in which researchers in
biology and cognitive science use the concept of 'communication' – based on a corpus
of over 1.1 million scientific papers across these fields. Individual points correspond to
paragraphs mentioning 'communication' and they are coloured and clustered according
to the "topic" which the model determined–picking out the specific research context in
which the central concept is employed, and allowing us to explore how its different uses
relate to one another.

{% capture fig1_caption %}A 2D UMAP visualization of vector embeddings of paragraphs discussing biological communication, clustered by the "topic" assigned by a BERTopic model. The visualization comes from my PhD dissertation, “Scale-Free Communication?...” Hover over a point to read the truncated paragraph; click a topic in the legend to show or hide it, and drag to zoom.{% endcapture %}
{% include figure-embed.html
   src="/assets/vis/2026/07/vis_documents-results-communication-def-separate-incl-nodups-50.html"
   height="780px"
   wide="true"
   caption=fig1_caption %}

There are a few reasons this might all sound familiar: topic modelling is closely related
to a broader family of methods inspired by a view called "distributional semantics". This
largely Wittgensteinian approach suggests that the meaning of words is encapsulated in
their use, and the use can be approximated by looking at word co-occurrences. This
allows encoding meaning as a vector in a multi-dimensional space (called "vector
embeddings"). While this might sound a bit abstract, these methods do provide a way of
measuring semantic relations. For instance, the difference between vectors for "dog"
and "dogs", and "cat" and "cats" should be identical, capturing the "meaning" of the
plural. Similarly, we can expect words like "continent", "island", "archipelago" to be more
closely related to one another than to words like "deadline", "submission", "review".
This approach is also the basis for large language models (LLMs).

LLMs themselves can be useful for digital philosophers too. They can offer
sophisticated ways of mathematically representing meaning of sentences and larger
documents. A recently proposed alternative to LDA topic modelling, BERTopic, relies on
clustering vector embeddings to identify "topics", whilst methods of "semantic
search" (identifying sentences and documents with similar vector embeddings) can be
used to identify papers or passages which refer to particular concepts, without relying
on keyword searches. The example of my own work, mentioned above, used semantic
search methods to uncover individual sentences and paragraphs which refer to the
notion of "biological communication". Such samples can then be used for conceptual
analysis, mitigating some of the risks associated with traditional case study use.

{% capture fig2_caption %}This image shows how vector representations calculated with LLMs can be used to construct a corpus of papers within the field of “language emergence”, based on a manually selected sample of prototypical “seed” papers. Here, we can cluster papers into a “field” despite a lack of things like specific journals or clear keywords for that discipline. The visualization (a 3D UMAP visualization of vector embeddings of full-text papers) comes from a study that will be presented at the Annual Meeting of the Cognitive Science Society 2026, preprint available at: https://doi.org/10.31234/osf.io/xjhya_v1. Drag to rotate, scroll to zoom, and use the legend to isolate a single group.{% endcapture %}
{% include figure-embed.html
   src="/assets/vis/2026/07/corpus_comparison_3d_umap.html"
   height="900px"
   wide="true"
   caption=fig2_caption %}

But digital methods are not a panacea: they enhance our abilities to study scientific
literature, but there are good reasons to worry about this focus on textual outputs of
science (not least that various publishing pressures strongly shape the content). That
said, publications can function as a strong factor in the reproduction of concepts,
theories, and practices. This is well captured within the cognitive approach to
philosophy of science, which allows for viewing publications as "cognitive artifacts",
serving a representational function, and affecting researcher's cognitive performance,
including in other dimensions of scientific practice (this view, emerging from the work of
Nancy Nersessian and Donald Norman, has been most explicitly formulated as
"cognitive metascience" by Marcin Miłkowski).

These methods can also be extended to datasets which relate to practice in different
ways, for instance, studies of peer reviews (something recently championed  by Marcin
Miłkowski). The same methods could be applied to other sorts of "grey" literature: lab
notebooks and reports, various tutorials, mailing lists, and so on. These textual records
are often subject to different pressures and so may reveal other dimensions of scientific
practice.

There are also non-epistemic challenges for digital approaches to philosophy, and the
humanities more broadly: notably, the existential risk that humanities at large currently
face, with academic funding being restructured to fit into narrowly understood
technological interests of some stakeholders. Almost exactly 10 years ago, Daniel
Allington, Sarah Brouillete, and David Golumbia published a critique which highlighted
how the arguments in favour of digital humanities follow the techno-optimistic rhetoric
of Silicon Valley and feed into the "neoliberal takeover of the university". Indeed, the
risks of techno-saviourism have never been more salient than now, when the
undemocratic, oligarchic control of increasingly popular technologies impacts not only
academic research, but also politics, the environment and many other aspects of our
lives. It is worth underscoring here, then, that digital tools do not secure any ideal of
"objective knowledge" for philosophy. Study design—as PSP-ers know well—involves a
host of (often arbitrary) methodological decisions which shape what quantitative results
those tools provide. Those results still need to be submitted to careful interpretation to
provide any relevant insights into philosophical questions. In many cases, such
interpretative procedures are the only tool for ascertaining the validity of results, as the
possibilities for statistical analysis in digital humanities are currently quite limited.

Happily, a vast majority of studies in digital philosophy use mixed-methods or multi-
level methodologies, which pair digital, quantitative analyses with a careful close
reading and conceptual analysis of the sample that qualitative methods provide. Digital
methods, then, are not here to replace the proverbial philosopher's toolbox, but rather
to expand and enhance it.
