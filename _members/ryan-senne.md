---
name: Ryan Senne
image: images/ryan-senne.jpg
role: phd
description: Neuroscience (GPN) PhD student, joint with Ben Scott
aliases:
links:
  email: rsenne@bu.edu
  twitter: ryan_senne
  github: rsenne
  website: https://ryguy.io
---

## Research

I am a computational neuroscientist, co-advised by Brian DePasquale and [Ben Scott](https://www.scottcognitionlab.com/). I build statistical models that infer the hidden states shaping behavior and neural activity, and I develop open-source tools that make these models easy to use.

### Diurnal rhythms of decision making

Decision strategies are not fixed. They drift with arousal, motivation, and time of day. Most state-dependent models of behavior track these shifts using choices alone and ignore reaction times. I developed a state-dependent drift diffusion model that couples a drift diffusion model with a hidden Markov model, using both choices and reaction times to infer when an animal switches strategy. Applied to rats performing a decision-making task around the clock, the model reveals time-dependent changes in decision making across the 24-hour day. I presented this work at COSYNE 2026, and the manuscript is in revision. The code lives in [DriftDiffusionModels.jl](https://github.com/depasquale-lab/DriftDiffusionModels.jl) and [24_Hour_Behavior](https://github.com/depasquale-lab/24_Hour_Behavior).

### Linking decision making to neuromodulation

Shifts in decision strategy likely reflect changes in brain state, and neuromodulatory systems are prime candidates for driving them. In collaboration with the [International Brain Laboratory](https://www.internationalbrainlab.com/) (IBL), I am developing models that relate changes in decision-making behavior to recordings from neuromodulatory systems. These include dopamine neurons in the ventral tegmental area (VTA) and substantia nigra pars compacta (SNc), norepinephrine neurons in the locus coeruleus (LC), serotonin neurons in the dorsal raphe, and cholinergic neurons in the basal forebrain. The goal is to connect fluctuations in neuromodulatory activity to the hidden states that shape an animal's choices and reaction times.

### Cross-species behavior in SHANK3 models

I am also analyzing behavior across marmosets, mice, and humans, comparing individuals with SHANK3 mutations to typically developing (TD) populations. SHANK3 is a synaptic gene whose loss causes Phelan-McDermid syndrome and is strongly linked to autism. The goal is to identify which behavioral differences are shared across species.

### StateSpaceDynamics.jl

I lead development of [StateSpaceDynamics.jl](https://github.com/depasquale-lab/StateSpaceDynamics.jl), the lab's fast, self-contained Julia package for latent state-space models. It covers Gaussian and Poisson linear dynamical systems, switching linear dynamical systems, and probabilistic PCA. Many models are trialized to match the structure of neuroscience experiments, but they apply to any sequential data. The package is described in a paper in the [Journal of Open Source Software](https://doi.org/10.21105/joss.08077) (Senne et al., 2025).

## Non-science biography

Outside of the lab, I’m a huge bookworm, cinephile, outdoorsman, and foodie. My favorite types of books and movies are philosophical. I currently have the entire history of western philosophy sitting on my bookshelf along with several novels and some neuroscience books. I like asking “the big questions” on life and I think books and movies are a great way of analyzing what it means to be human. When I don’t have my nose crammed in a book I like to be outdoors. Growing up in Minnesota gave me a vast appreciation for the great outdoors. I’m as stereotypical outdoorsy as you can probably get. There just really isn’t any greater ecstasy than nature. Above all else, I enjoy the gluttonous side of life. Food is such an integral piece of human culture that I taught myself how to cook. I enjoy sharing my passions for cuisine and coffee with all of my friends. The best dish I can probably cook is beef bourguignon or my spaghetti carbonara. Something I think we can all enjoy is a nice meal with a stiff glass of espresso to wash it down.