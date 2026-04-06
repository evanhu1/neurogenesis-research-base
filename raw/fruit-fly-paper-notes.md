Fruit Fly Brain Paper

- Real biological neural circuits are actually remarkably robust to parameter
  variation. The work of Eve Marder on the crustacean stomatogastric ganglion
  found that the same rhythmic motor pattern — the same functional output — can
  be produced by wildly different combinations of ion channel conductances,
  synaptic strengths, and cellular properties across individual animals. Two
  lobsters can have the same stomach churning rhythm but completely different
  underlying parameter sets. The system is degenerate: many parameter
  configurations map to the same functional behavior. Evolution tends to find
  solutions that sit in broad, flat regions of parameter space rather than on
  narrow peaks. I want to find a similar design for Neurogenesis.
- A first-order neuron is the sensory neuron itself — the GRN that directly
  detects the stimulus. A second-order neuron is one synapse away: it receives
  direct synaptic input from the sensory neuron. Third-order is two synapses
  away, and so on. In the feeding circuit, the layout is: GRNs
  (first-order/sensory) → neurons like Zorro, Clavicle, G2N-1, Usnea
  (second-order) → neurons like Sternum, Bract (third-order) → premotor neurons
  like Roundup, Roundtree (which you could call fourth-order) → MN9 (motor
  output).
- In simpler brains circuits are mostly direct sensorimotor reflex arcs that
  flow feedforward from sensory to motor. In humans there is massive recurrence
  and feedback.
- Disinhibition is one of the most fundamental and ubiquitous circuit motifs in
  the brain. It implements conditional gating, which excitatory circuits cannot.
  The basal ganglia, which control action selection in all vertebrates including
  humans, are essentially a giant disinhibition machine.
- Recurrent excitation, where neurons excite each other in a loop. This can
  sustain activity after the initial input is gone (working memory), amplify
  weak signals, or create attractor states
- Feedforward inhibition, where a sensory input simultaneously excites an
  excitatory neuron and an inhibitory neuron that also targets the excitatory
  neuron. The inhibition arrives slightly after the excitation (because it goes
  through one extra synapse), creating a brief window of excitability followed
  by suppression. This sharpens the temporal precision of responses — the neuron
  fires a brief, precisely timed burst rather than a prolonged response. This is
  heavily used in auditory processing where timing matters.
- Negative feedback, where a neuron's output, through an inhibitory
  intermediary, suppresses its own input. This prevents runaway excitation and
  keeps firing rates in a stable operating range. It's homeostatic
- Can vary inhibitory:excitatory ratio by adding a multiplier to the inhibitory
  weight effect.
- In human brains the max neuron order is roughly 10–20 synapses from sensory
  receptor to the highest association areas
- Without feedback, the brain would be a purely reactive feedforward pipeline:
  stimulus in, response out, no internal model, no predictions, no flexible
  attention, no memory. Essentially a lookup table. Feedback is what makes the
  brain a dynamical system rather than a static function.
- Brain developmental program is a compression problem. The human genome has
  about 20,000 protein-coding genes. The brain has roughly 86 billion neurons
  with an estimated 100–500 trillion synapses. You cannot specify each synapse
  individually in the genome — you're off by about 10 orders of magnitude. The
  genome doesn't contain a wiring diagram. It contains a program — a set of
  rules that, when executed in the context of the developing embryo, produces a
  brain. Program: 1. Signal molecule (morphogens and transcription factors)
  gradients establishes regional patterning. 2. Neurogenesis. Within each region
  progenitor cells mass produce neurons on stereotyped schedules. 3. Axon
  guidance relies on molecular cues (attractants and repellents) distributed
  throughout the brain to guide neuron axon growth tips to find their targets.
  guidance cues don't specify individual connections — they specify classes of
  connections. "Motor cortex axons, go to the spinal cord" is a rule that
  applies to millions of axons simultaneously, encoded by a handful of guidance
  molecules. Topographic maps (like the retinotopic map from retina to visual
  cortex) are established by gradients of ephrins, where the position of a
  neuron's cell body in one area maps smoothly to the position of its axon
  terminal in the target area. One gradient pair creates an entire ordered
  map. 4. Synaptogenesis. Axons once in their target area, use cell-surface
  recognition molecules — enormous families of proteins like protocadherins,
  neurexins, and neuroligins — to distinguish appropriate from inappropriate
  partners. Each neuron expresses a nearly unique surface identity from a modest
  number of genes, which is thought to mediate self-avoidance (a neuron's own
  dendrites repel each other to spread out evenly) and possibly partner
  matching. 5. Refinement. The initial wiring established by molecular cues is
  coarse and imprecise. Then, neural activity — first spontaneous waves of
  activity in utero, then sensory experience after birth — sculpts the circuit.
  Synapses that are functionally appropriate (their activity correlates with the
  postsynaptic neuron's activity) are strengthened and stabilized. Synapses that
  are inappropriate (uncorrelated activity) are weakened and eliminated. This is
  competitive and self-organizing: the circuit tunes itself through use. Mainly
  two mechanisms: 6. Selective cell death (apoptosis). The brain initially
  overproduces neurons, then removes many of them through regulated cell death.
  A major mechanism is trophic competition: neurons compete for limited survival
  signals from targets and surrounding tissue, and those that fail to secure
  enough support activate intrinsic apoptotic programs and die. This matches
  neuron number to target size and eliminates poorly integrated cells. 7.
  Pruning. Surviving neurons also begin with excess axon branches, dendrites,
  and synapses, many of which are later removed. Pruning is driven by molecular
  signals and neural activity: weaker, less correlated, or less competitive
  connections are selectively destabilized and eliminated, while stronger,
  functionally useful ones are retained. The neuron survives, but its
  connectivity is sculpted down. The genome specifies the general plan — the
  regional organization, the cell types, the major axon pathways, the target
  zones for synapse formation
- In the Flywire connectome, each pair of connected neurons has a weight equal
  to the number of synapses between them. These synapse counts vary — some
  neuron pairs are connected by 1 synapse, some by 5, some by 50, some by
  hundreds. If you made a histogram of all connection weights in the entire
  brain, you'd get a distribution — probably something right-skewed, with many
  weak connections and fewer strong ones.
- Homeostatic Plasticity is a key source of robustness in the brain, across
  neuron types, different have different preferred spiking rate rangesExcitatory
  pyramidal neurons in cortex homeostatically maintain rates of roughly 1–10 Hz.
  Fast-spiking inhibitory interneurons maintain much higher rates, often 20–60
  Hz. They tune their own excitability to stay within their preferred range.
  This range is set in the genome.
- Dale’s Law is still a reasonable rule
