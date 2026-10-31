---
name: Ryan Senne
image: images/ryan-senne.jpg
role: phd
description: Neuroscience (GPN) PhD student, joint with Ben Scott
aliases:
links:
  email: rsenne@bu.edu
  bluesky: ryguy.io
  github: rsenne
  google-scholar: IwC7mqEAAAAJ&hl=en
  orcid: 0000-0003-3776-4576
  website: https://ryguy.io
---

## Research

I am a computational neuroscientist, co-advised by Brian DePasquale and [Ben Scott](https://www.scottcognitionlab.com/). I build statistical models that infer the hidden states shaping behavior and neural activity, and I develop open-source tools that make these models easy to use.

### Diurnal rhythms of decision making

Decision strategies are not fixed. They drift with arousal, motivation, and time of day. Most state-dependent models of behavior track these shifts using choices alone and ignore reaction times. I developed a state-dependent drift diffusion model that couples a drift diffusion model with a hidden Markov model, using both choices and reaction times to infer when an animal switches strategy. Applied to rats performing a decision-making task around the clock, the model reveals time-dependent changes in decision making across the 24-hour day. I presented this work at COSYNE 2026, and a [preprint](https://doi.org/10.21203/rs.3.rs-9883645/v1) is available. The code lives in [DriftDiffusionModels.jl](https://github.com/depasquale-lab/DriftDiffusionModels.jl) and [24_Hour_Behavior](https://github.com/depasquale-lab/24_Hour_Behavior).

### Cross-species behavior in SHANK3 models

I am also analyzing behavior across marmosets, mice, and humans, comparing individuals with SHANK3 mutations to typically developing (TD) populations. SHANK3 is a synaptic gene whose loss causes Phelan-McDermid syndrome and is strongly linked to autism. The goal is to identify which behavioral differences are shared across species.

### Linking decision making to neuromodulation

Shifts in decision strategy likely reflect changes in brain state, and neuromodulatory systems are prime candidates for driving them. In collaboration with the [International Brain Laboratory](https://www.internationalbrainlab.com/) (IBL), I am developing models that relate changes in decision-making behavior to recordings from neuromodulatory systems. These include dopamine neurons in the ventral tegmental area (VTA) and substantia nigra pars compacta (SNc), norepinephrine neurons in the locus coeruleus (LC), serotonin neurons in the dorsal raphe, and cholinergic neurons in the basal forebrain. The goal is to connect fluctuations in neuromodulatory activity to the hidden states that shape an animal's choices and reaction times.

### StateSpaceDynamics.jl

I lead development of [StateSpaceDynamics.jl](https://github.com/depasquale-lab/StateSpaceDynamics.jl), the lab's fast, self-contained Julia package for latent state-space models. It covers Gaussian and Poisson linear dynamical systems, switching linear dynamical systems, and probabilistic PCA. Many models are trialized to match the structure of neuroscience experiments, but they apply to any sequential data. The package is described in a paper in the [Journal of Open Source Software](https://doi.org/10.21105/joss.08077) (Senne et al., 2025).

## Publications and presentations

### Publications

- **Senne, R.A.**, Suthard, R.L., Cao, R., Coello, S., Monasterio, A.H., Ruesch, E.A., Buzharsky, M.D., Howard, M.W., Ramirez, S. (2026). *Hippocampal astrocytic sequences emerge during learning and memory recall.* Nature Neuroscience. [doi](https://doi.org/10.1038/s41593-026-02448-0)
- **Senne, R.A.**, Xia, H., Duebel, H.F., Do, Q., Kane, G.A., Fourie, J., Ramirez, S., Scott, B.B., DePasquale, B. (2026). *Diurnal rhythms of choice: a novel state-dependent drift diffusion model uncovers time-dependent changes in rat decision making.* Research Square. [preprint](https://doi.org/10.21203/rs.3.rs-9883645/v1)
- **Senne, R.A.**, Loschinskey, Z., Fourie, J., Loughridge, C., DePasquale, B. (2025). *StateSpaceDynamics.jl: A Julia package for probabilistic state space models (SSMs).* Journal of Open Source Software 10(115): 8077. [doi](https://doi.org/10.21105/joss.08077)
- **Senne, R.A.**, Delgado-Sallent, C., Ramirez, S., Scott, B.B., DePasquale, B. (2025). *A state-dependent drift diffusion model reveals mice actively explore a speed-accuracy continuum during decision-making.* bioRxiv. [preprint](https://doi.org/10.1101/2025.06.02.657156)
- Kane, G.A., **Senne, R.A.**, Scott, B.B. (2023). *Rat movements reflect internal decision dynamics in an evidence accumulation task.* bioRxiv. [preprint](https://doi.org/10.1101/2023.09.11.556575)

### Presentations

- **Senne, R.A.**, Duebel, H., Fourie, J., Scott, B., DePasquale, B. (2026). *A State Dependent Drift-Diffusion Model Identifies Circadian Decision Dynamics.* Cosyne 2026, Lisbon, Portugal.
- **Senne, R.A.**, Loschinskey, Z., Loughridge, C., Fourie, J., DePasquale, B. (2025). *StateSpaceDynamics.jl: Probabilistic State-Space Modeling.* JuliaCon 2025, Pittsburgh, PA. [talk page](https://pretalx.com/juliacon-2025/talk/DJTA7U/)

## Non-science biography

Outside of the lab, I’m a huge bookworm, cinephile, outdoorsman, and foodie. My favorite types of books and movies are philosophical. I currently have the entire history of western philosophy sitting on my bookshelf along with several novels and some neuroscience books. I like asking “the big questions” on life and I think books and movies are a great way of analyzing what it means to be human. When I don’t have my nose crammed in a book I like to be outdoors. Growing up in Minnesota gave me a vast appreciation for the great outdoors. I’m as stereotypical outdoorsy as you can probably get. There just really isn’t any greater ecstasy than nature. Above all else, I enjoy the gluttonous side of life. Food is such an integral piece of human culture that I taught myself how to cook. I enjoy sharing my passions for cuisine and coffee with all of my friends. The best dish I can probably cook is beef bourguignon or my spaghetti carbonara. Something I think we can all enjoy is a nice meal with a stiff glass of espresso to wash it down.