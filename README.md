# Master's of Engineering Thesis for Austin Garrett

Proposal draft (v0.1)

Bayesian Inference over Structured Scenes from Image Data

Intro

Hook: The past decade has seen a flourishing of highly powerful computer vision
techniques, due to the success of deep learning techniques accelerated on
massively parallel hardware.

Gap: Yet the shortcomings of neural techniques have only grown increasingly
urgent in proportion to their dominance. While these approaches have resulted
in the amortization of traditionally very difficult and high-dimensional
computer vision problems, the lack of semantic structuring in their output has
led to great challenges in their deployment in practical domains where
interpretability and composability are desperately needed to integrate these
components into larger frameworks.

Motivation: Meanwhile probabilistic techniques offer a more principled approach
to modeling structured data, and have seen a rapid growth in the collective
ecosystem. Such environments are desirable for their expressibility,
corresponding to the fact that they often represent intuitive models of
rationality inspired from cognitive and neuroscience which increasingly rely on
such modeling to explain the human reasoning.

Related Works

    Neural Approaches
        Deep Object Pose Estimation
        PoseCNN

    Bayesian inference over structured scenes
        Contact Graph Representation
            FIG: Contact graph representation (maybe from Ben's poster?)
        NeurIPS 2019 Workshop
            FIG: NeurIPS figure
        LAFI 2019
            FIG: LAFI figure

Proposed Works

    Time Table

    FIG: Bayes' net diagram 
        SUBFIG A: static structure, dynamic parameters
        SUBFIG B: dynamic structure, dynamic parameters

    Composing Neural Techniques with Generative Modeling

    Fixed scene structure, dynamic parameters

    Dynamic scene structure, dynamic parameters
        Reversible jump MCMC

    Engineering Infrastructure
        FIG: ROS infrastructure diagram
        Realtime Particle Filtering
        Visualization
        Cora Project (perhaps place something in related works as well?)

    NeurIPS 2020 Journal Submission/Extensions to work
        Possible direction #1 - Placeholder
        Possible direction #2 - Placeholder
        Possible direction #3 - Placeholder


BIG IDEAS

\subsection{Neuro-Symbolic Predictive Coding OR Generative Modeling for Neuro-Predictive Error Correction}

In some ways the current state-of-the-art in both neural and probabilistic
techniques have orthogonal and complementary strengths and weaknesses. While
neural techniques exhibit strong performance in parsing out useful statistics
from massively high-dimensional data with relatively little compute, they
struggle to enforce semantically meaningful constraints on those statistics. On
the other hand, probabilistic techniques can naturally capture symbolic systems
and thus are much more expressible when it comes to representing and reasoning
about highly structured semantic content. However, the dominant paradigms for
inference treats it mostly as a top-down problem in which latent scene
parameters are estimated via mostly-blind random walks. This "guess-and-check"
methodology creates a bottleneck in propagating information from low-level
features to the statistics of interest.

We believe there is a natural road to combining the strength of these two
approaches. We propose a compositional technique where each system is used to
leverage its own abilities. We propose 

This corresponds to a meta-modeling predictive coding problem, in which we
represent and abstract the behavior of the black-box neural model with a
generative model that leverages the intuition we have about the failure modes
of these neural systems. Our generative procedure is not attempting to predict
the images themselves, but rather construct a robust model of the detector
itself in order to enrich the unstructured and noisy outputs of the detector
with structured information.

There is also a possible path to a more fully distributed set of models, via a
reformulation of the inference procedure as 

PROPOSED FIGURE: A spurious DOPE detection is pictured. Below, the abstract
scene graph is visualized, along with a percentage of occlusion. The more
abstract model captures this via increasing the uncertainty of the pose
estimation.

