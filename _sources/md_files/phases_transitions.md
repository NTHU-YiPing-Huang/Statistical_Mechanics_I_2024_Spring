# Phases and phase transitions

*Reference: {cite:p}`goldenfeld2018lectures` Chap. 2,3,5*

```{admonition} Summary
:class: tip
1. A phase means a stable pattern of a collective behavior for a many-body system.
2. A phase diagram is the diagram defined in the parameter space of a particular Hamiltonian. Different points on the diagram represent different parameters of the corresponding Hamiltonian. Points in the same regrion are the points in the same phase.
3. Phase transitions occurs when the pattern of the collective behavior of the many-body system changes. The pattern could change adruptly or slowly. The sudden change of collective behavior is called the discontinuous phase transition. The smooth change of collective behavior is called the continuous phase transition.
4. Thermodyanmic limit matters for a well-defined notion of phase transition.
5. Spontaneous symmetry breaking means the Hamiltonian of the system has a symmetry. But the statistical behavior of the system does not respect that symmetry. It is an emergent phenomenon!
6. The phases and phase diagram of Ising model
	* The thermal fluctuation at one-dimensional Ising model melts the order. No finite temperature phase transition in one-dimensional Ising model.
	* The thermal fluctuation at two-dimensional Ising model is not so strong, so there is a finite temperature phase transition for the two-dimensional Ising model.
7. We can solve one-dimensional Ising model using the transfer matrix method.
8. Mean field theory is a versatile and simple approach for interacting systems.
	* It can be directly connected with the physical picture.
	* It does not have the information of dimensionality.
	* It can be qualitative wrong. For example, it predicts a finite temperature phase transition for the one-dimensional Ising model which has no finite temperature phase transition according to the exact result using the transfer matrix approach.
9. The mean field theory is closely related to the physical picture of Ginsburg-Landau theory.
```

## Motivation

### Why should we study phases of matter and phase transitions?

From the broad scope, why studying phases of matter is important? The simplest reason for this course is: we would like to extend our understandings beyond interacting free systems, since most of the systems in nature are interacting systems. The non-interacting limit is just a pedagogical limit. We have learned the fundamental structure of statistical mechanics and use it to study several interacting free systems. It is about time to explore the more challenging interacting systems. 

The interacting free systems are nice since we can reduce the many-body problem into a single body problem. Why it is so? When the degrees of freedom are not interacting with each other, we can effectively consider the physics for any one of the "free modes". Since the "free modes" does not talk with each other, understanding one of them is equivalent to understand all of them. (Like the Debye model, $\omega(k_1)$ and $\omega(k_2)$ mode has no fundamental difference.) That behavior is also demonstrated in the fact that we can factorize our partition function easily.

We can try to imagine what will be different if we include interactions. At the non-interacting limit, the collective modes does not couple with each other. When those modes interact with each other in some way, there are at least two possibilities. The first possibility is the interaction between those modes does not change the behavior of the system qualitatively. Some minor detail is modified, we can adjust the description and, again, describe the system formally as a non-interacting system (interaction is an irrelevant coupling, in renormalization group language). The other possibility which is more interesting. The coupling between these modes might be modified dramatically by the interaction such that the new collective mode cannot be approximated by the non-interacting modes we start with (interaction is a relevant coupling, in renormalization group language). The pattern of collective behavior could be changed qualitatively and new phenomena emerge. The new phenomena  might be difficult to be understood using the non-interacting variables, we might need to develop new theories to describe the essence of them.

### The pattern of collective behavior

**Studying phases is studying the patterns of collective behavior. Studying phase transitions is exploring how patterns of collective behavior changes under distinct circumstances.** It is tempting to ask: if we change the form of the interaction (from non-interacting to interacting) or if we change the constraints of the interaction (interaction can happen only when certain condition is satisfied), how the pattern of collective behavior changes? This is the type of questions we address on the research of phase transitions. For example, the transition from the paramagnetic phase to the ferromagnetic phase of the Ising model. The paramagnetic phase is a phase where the spins are arranged randomly. We can ask: if we turn on a "weak"(weak comparing with what?) coupling between the spins, will that modify the behavior of the spin once an infinite small interaction is turned on? Intuition tells us that it should not be the case, the paramagnetic phase should survive until the interaction between the spins are too strong such that they can overcome the thermal fluctuation. Therefore, the paramagnetic phase for non-interacting spins and the paramagnetic phase of weakly interacting spins should be considered as qualitatively similar pattern of collective behavior. We will discuss related phenomena deeper during the lectures.

The simple phenomena described above already raises an important question: how to describe a phase? What is a scientific sound definition of a phase? What can we say about the corresponding phase transition according to this definition? That leads to a deeper question we would like to answer during the study of phases and phase transitions. *i.e.* What is the theoretical framework to describe the pattern of collective behavior such that it is coarse enough to identify those patterns without qualitative difference and sharp enough to signal the subtle difference between those patterns with quantitative distinct physical properties? Different levels of answers of this question will be the stepping stones to the important concept of effective theories.

### Effective theory at different scales

To be more concrete, once we understand more or less what is a phase and how phase transition happen in principle, it is very tempting to ask: when one goes from phase A to phase B via a phase transition, are there any relation between the two phases, *i.e.*, phase A and phase B? The question is strongly related to **HOW** the many-body system changes the pattern of collective behavior? If there is a specific mechanism behind the phase transition, maybe we can bridge the relation between phase A and phase B. Maybe in the other phases, phase C and phase D could also go from one to the other using similar mechanism. If so, can we build some kind of equivalence relation saying the phase transition from phase A to phase B is similar with the phase transition from phase C to phase D? If it is possible, can we find a unified framework to understand or to categorize those transitions? Also, what is the relation between the theory describe phase A and the theory describe phase C, are they also related in some way? It turns out, it is related to the concept of renormalization group which also leads to the [Nobel prize of K. G. Wilson](https://www.nobelprize.org/prizes/physics/1982/wilson/lecture/). Basically, **the concept of renormalization group provides a framework to categorize theories, therefore, the concept provides "a theory of theories". It is the foundation of the effective theory approach.**

The line of thought is not emphasized in the undergraduate courses. The four "mechanics" of physics department are: classical mechanics, quantum mechanics, electromagnetic dynamics and statistical mechanics. Statistical mechanics is the only one that focuses on systems with many-degrees of freedom and does not have a specific "applicable region". (Classical mechanics works in the "classical world", quantum mechanics works in "atomic world", electromagnetic dynamics discussed charged system in the "classical world" or the "atomic world".) At the first glance, it seems like it is not as fundamental with the others. We consider the microscopic physics being governed by classical mechanics, quantum mechanics and electrodynamics. Then we study those system via statistical mechanics. It seems like we just apply the more "fundamental" physics laws to the many-body system. Why it is a required course for the physics department?

One of the reason that it is not obvious to appreciate this subject is because we need to start from something simple: we usually start with interacting free system. It is difficult to unleash the full potential of statistical mechanics. The study of phases, phase transitions and critical phenomena provides a very nice platform to introduce those fantastic ideas. Especially when interacting effect is included. However, due to the time limit, we will not be able to cover those amazing concepts this semester. We will discuss those ideas in more detail in the Statistical Mechanics (II).


## The spirit of model studying

In the study of phases or phase transitions, one will encounter various models. Ising model, Heisnberg model, Potts model, dimer models, height models, etc. They are related to various interesting concepts including topology and gauge theories. However, why should we study those models? What can we learn from studying of those models?

We will discuss one of the important models -- the Ising model. After we study the Ising model, one will soon realize that the model are quite ''simple''. It is so simple that it is not clear why such a simple model would be relevant to describe our nature. Other above mentioned models also share similar features that they seem to be ad hoc models for special purposes. There should be some physical arguments about why we should study such models and how such ad hoc models could help us understand certain physical phenomena.

Conceptually, it is tied with the idea that we are looking for a simplest nontrivial model to help us understand specific physical phenomena.
From this perspective, the Ising model is the simplest non-trivial model to study phase transitions.
To study phase transitions, at least the model needs to have two phases.
Ising model host a disordered phase at high temperature and a ordered phase at zero temperature limit. 
Surprisingly, Ising model also demonstrate two types of phase transitions: the first order phase transition and continuous phase transition depends on whether the $Z_2$ symmetry is explicitly broken. 
However, with only discrete symmetry, we don't expect Ising model to demonstrate the behavior of phase transition with continuous symmetry.
To study those phenomena, one needs to find a simplest nontrivial model with continuous symmetry.

We describe the model as 'simple' models in a sense that the physical meaning and the expression of the model can be related clearly. But that does not mean they are easy to study or understand. However, because of the 'simplicity', one can go pretty far to understand those models. Sometimes, one can even solve it exactly.

On the other hand, one could feel studying those models are usually far away from physical reality.
How could such highly simplified models gives us hints about what happened in nature? The traditional approach is to start from microscopic physics and include different effects one by one.
If certain phenomena is not captured, we include more parameters into our model.
Such bottom up approach usually have very strong connection with microscopic details.
However it usually also leads to a complicated Hamiltonian which can only be solved approximately.
Comparing with the idealistic models which can be solved exactly, one might reach the conclusion that we should just give up those beautiful structure and use computers to help us solving those complicate but realistic model.

The problem about this approach is about the generality. Starting from realistic but complicate models, one can make some predictions. Or even fit the experimental data pretty well by tuning parameters. However, what is the general structure for the model is usually hidden behind the complicated competing effects. The simple toy models might not give us quantitatively correct answers. However, the simple structure helps us to identify the universal behavior and the mechanism behind the universal behaviors.

From this point of view, studying those simple but nontrivial models actually is quite valuable to understand the general behavior without the microscopic details. However, how to get the simplest non-trivial model as a starting point is an art. The theoretical framework that address this question is the concept of renormalization group(RG) and effective theory. One can use RG to identify the relevant ingredients for constructing a simplest non-trivial model. The two approach has their pros and cons, one should keep that in mind and use them according to different purposes.

## Ising model--The simplest non-trivial system

It is amazing that Ising model teaches us so many things including the physics of phases and phase transitions. It is crucial to build a physical picture about what is a phase and what are the corresponding phase diagram from a simple system that we can grasp the key concepts. Therefore, we will focus on the phases and phase diagram of the ferromagnetic Ising model with nearest-neighbor interaction on hypercubic lattices.

We will start with heuristic physical arguments to understand the phases and phase diagram. During the argument, we can observe the close relation between dimensionality and the strength of fluctuation. Then, we will switch to the more formal approach to derive the partition function of Ising models. In one-dimensional Ising model with external field, we will introduce the transfer matrix method which can give us the exact expression of the partition function. Unfortunately, the approach cannot be generalize to higher dimension. Therefore, we will introduce the mean-field approach which is more versatile but still with its own limitation. Hopefully, in the last lecture, we could introduce the Ginsburg-Landau theory and leave it as a teaser for the more advanced concept such as renormalization group and its connection with critical phenomena and universality class. Those interesting topics will be discussed in the next semester course of statistical mechanics (II).

