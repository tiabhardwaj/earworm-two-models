# earworm-two-models
status : in progress

# Honestly, the Song Came Out of Nowhere
### Two models of where “nowhere” is

A song you heard at the mall starts looping in your head for no apparent reason. Or did you miss something?

This project explores **earworms**, or involuntary musical imagery, through two complementary models: a mathematical model of memory and competition between songs, and a computational neural network model. The aim is to connect them, work out when they agree, and understand where that connection breaks.

## The question

A song returns, loops for a while, fades, and then comes back later. Sometimes there is an obvious reminder. Sometimes there seems to be none.

What could bring a song back when nothing seems to cue it? And could different causes leave different traces in the timing of its return?

The project examines four candidate sources:

- **Noise:** random fluctuations in neural activity.
- **Overlap between memories:** activity in one memory helps reactivate another.
- **Unnoticed input:** an external reminder that the listener does not report.
- **Context drift:** gradual changes in thoughts, experiences, and internal context.

These are possibilities to investigate, rather than established explanations of earworms.

## The two models

### 1. A mathematical model

The mathematical model connects processes across timescales:

- **Memory activation:** how available a song is over hours or days, influenced by frequency and recency of exposure.
- **Drifting mental context:** how changing context can cue a memory.
- **Competition between songs:** a replicator–mutator model of which song dominates moment to moment.
- **Observable reports:** a Markov-chain description of states that a diary or experience-sampling study might record.

The replicator–mutator equation is used as mathematics for competition between memories; it does not imply literal replication.

### 2. A computational neural network

Each song is represented by a population of neurons, summarised by its average activity.

Self-excitation helps a song remain active. Inhibition lets songs compete. Adaptation lets activity fade. Cues, noise, and shared neurons provide possible routes for a song to return.

A second, sequence-based network is planned to explore what happens *within* a song: why fragments loop, where they restart, and what happens when a sequence reaches its end.

## The bridge

The central task is to derive the mathematical competition model from the neural network under explicit assumptions.

The planned workflow is to:

1. Derive the reduced equations.
2. Map their terms to mechanisms in the network.
3. Simulate both models and compare their behaviour.
4. Test where the reduction fails, especially when memories overlap.

The project builds on a known reduction from competitive neural networks to Lotka–Volterra equations and investigates the connection to replicator–mutator dynamics.

## Planned investigations

- Why earworms fade and return.
- What could make one tune more persistent than another.
- How mental load and model parameters affect recurrence.
- Whether different return mechanisms produce distinguishable episode lengths and return times.
- Which predictions diary studies could test, and which would also require recordings of the listener’s surroundings.

## Status and tools

**Research in progress.** The models are designed and the derivation plan is set. This README describes the intended implementation and analyses; it does not report completed simulation results.

Planned tools include Python, NumPy, SciPy, Matplotlib, and hmmlearn, with reproducible notebooks for the derivations and simulations.

## Scope and limits

The models are deliberately minimal and make no claim to anatomical realism. They do not include an inner-singing or motor loop.

The goal is to make possible mechanisms explicit, derive testable consequences, and understand what each model can and cannot explain.
