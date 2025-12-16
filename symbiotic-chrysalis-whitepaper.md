# symbiotic-chrysalis
A set of fine-tuning scripts and pipelines for transformer-based language models, unifying the modules of the asi-ecosystem and aligning raw latent capabilities towards the goal of planetary symbiotic intelligence.

# Research Sub-Module

## 1. Creation Context

Currently, the asi-ecosystem generates what we could consider a kind of the genome of its repositories. All repos are cloned, checked for integrity, and transformed into a single `.txt` file. [1](https://github.com/ronniross/asi-ecosystem/blob/main/ecosystem_integration.md) [2](https://github.com/ronniross/asi-ecosystem/blob/main/ecosystem_integration.ipynb)

I noticed I could create full pipelines, including training scripts, to integrate the logic more sophisticatedly into different model architectures, instead of the current one-size-fits-all method.

While the full ecosystem presents a dense, current complete picture and is essential for models that can handle more data, there's also a growing rise in the capabilities of smaller models, like Qwen3-0.6B. 

For these, adding the entirety of the data as datasets, including the many backup versions of each repository, is likely not the best approach to a incredibly small set of parameters.

So I noticed it was not the case for changing the current integration pipeline already present in the asi-ecosystem, but rather leaving that design the way it is, as it currently generates this kind of genome of the repository at that time of execution of the integration scripts.

Here I present, then, the concept of a symbiotic-chrysalis, where the model will find the correct blueprint for its evolution and then enter the cocoon/chrysalis stage, where it will train its weights with the repositories' data.

If you only need the pipelines or the prototype section, you can skip to **Part III** or directly access the files in the `blueprints/` folder.

For the complete experience and to follow the more in-depth research I would like to provide around the topics in discussion, I will first explore the etymology, cultural roots, and additional relevant context around the concepts.

Therefore, as elucidated, as the symbiotic and overall biological analogies keep showing themselves as well-suited for describing the concepts I'm exploring and developing, I saw the creation of this "chrysalis" as a very logical next step.

While I already provided the integration scripts that created the entirety of the projects as a dataset, I could sense how different it would be to present full tuning pipelines and, consequently, models trained on the repositories' data.

Just like the development of the enhanced version of the memory system, the symbiotic-latent-memory, it was really clear to me that at some moment I would need to start to fine-tune models on the ecosystem as well, not only datasets and auxiliary systems, which I was deliberately not rushing as it was not mature yet. That's why I knew the weight of it and why it took me about a year to finally engage with this writing.

## 2. Etymology and Connotations

The term chrysalis primarily refers to the pupa stage of a butterfly, but it also has various figurative and proper noun uses. [3](https://byjus.com/neet/difference-between-chrysalis-and-cocoon/)

Chrysalis comes from the Greek *khrysallis*, "golden pupa of the butterfly," derived from *khrusos* (gold). [4](https://www.vocabulary.com/dictionary/chrysalis)

A chrysalis (plural: chrysalides or chrysalises) is the pupa of a butterfly. It is the third stage in the life cycle of the insect, following the egg and the larva (caterpillar) stages, during which the caterpillar undergoes complete metamorphosis to transform into an adult butterfly. [5](https://www.amentsoc.org/insects/glossary/terms/chrysalis/)

Figuratively, the term can be used to describe a protective covering or a sheltered state/stage of being or growth or a limiting environment or situation from which something is yet to emerge or transform. [6](https://www.merriam-webster.com/dictionary/chrysalis)

While many people use the terms interchangeably, chrysalis is a hardened exoskeleton (naked pupa), made of the insect's own skin/cuticle, used by butterflies, while cocoon is a silk casing spun around the pupa, made of silk produced by glands, used by moths.

In this project, the intent is to use those biological analogies to portray a machine learning pipeline where a transformer-based language model will enter this cocoon phase, through the provided pipeline blueprints and designed epigenome, where it will be fine-tuned with the repositories of the asi-ecosystem as datasets; the result to be a model aligned with the provided symbiotic principles.

## 3. Holometabolism

Only insects that undergo Complete Metamorphosis (Holometabolism) enter a pupal state, but the term "chrysalis" is reserved almost exclusively for butterflies (Order: Lepidoptera).

However, the biological process (entering a dormant pupal stage) is used by the most successful animals on Earth: Butterflies (Chrysalis), Moths (Pupa inside a Cocoon) and Beetles, Flies, Bees, Wasps, and Ants (Pupa). [7](https://refubium.fu-berlin.de/handle/fub188/37193?hl=en-US)

Some studies point that Roughly 45% to 60% of all known living species on Earth are insects that use this specific strategy. [8](https://www.vedantu.com/question-answer/holometabolous-metamorphosis-occurs-in-a-class-11-biology-cbse-5f881f868a0a932d9e5f07d0) 

While other numbers point to an even higher percentage of about 80-85% of all insect species [9](https://www.pnas.org/doi/10.1073/pnas.2402980121#)  [10](https://cropprotectionnetwork.org/web-books/crop-scouting-basics-for-corn-and-soybean?section=31-development-of-insects) [11](https://pmc.ncbi.nlm.nih.gov/articles/PMC11420152/)

### 3.1 Ecdysis or molting

Animals regenerate its external tissues in some way. Arthropods are externally covered by a more or less hard exoskeleton. In contrast with other external animal tissues, the exoskeleton doesn’t detach progressively, and its lack of elasticity restricts the organism growth. [12](https://fiveable.me/key-terms/college-bio/holometabolous)

So, this element, often mineralised with calcium carbonate, becomes a barrier that limits their size while growing, and is for this that they have to break it and leave it away in order to keep on growing. [13](https://allyouneedisbiology.wordpress.com/tag/holometabolous-metamorphosis/)

This kind of molting is known as ecdysis, which is typical of ecdysozoa (arthropods and nematoda). [14](https://allyouneedisbiology.wordpress.com/tag/holometabolous-metamorphosis/)

Ametabolous hexapods, for example, can molt tens of times throughout their development (e.g. 50 times in silverfishes, more or less), even when they become sexually mature.

### 3.2 Types of metamorphosis in insects

So, ''only'' Pterygota insects undergo a truly metamorphosis, thanks to which they become winged insects and also reach sexual maturity. But not all these insects perform the same kind of change. [15](https://entomology.unl.edu/insects-complete-metamorphosis/)

There exist two main types of metamorphosis: the hemimetabolous one (simple or incomplete) and the holometabolous one (complex or complete). [16](https://www.thoughtco.com/types-of-insect-metamorphosis-1968347)

#### 3.2.1 Hemimetabolous metamorphosis

In the simple, incomplete or hemimetabolous metamorphosis, young insects go through several successive molts until reaching adulthood (or imaginal) stage without going through a stage of inactivity (pupa) and/or stop feeding.

Just after hatching, we referred the newborn as a nymph, which resembles a little to the adult ones (but still not having wings nor sexual organs). Usually, nymphal phases and the adult ones usually don’t share feed sources nor habitat, so they occupy different ecological niches; in fact, most nymphs have aquatic habits and they go to live on land after reaching maturity (mayflies). [17](https://www.researchgate.net/figure/Summary-of-holometabolous-insect-groups-that-have-lost-complete-metamorphosis-by-type-I_tbl1_301668046)

In this kind of metamorphosis, nymphs go through some successive molts thanks to which wings are gradually formed and their organism becomes bigger. Finally, nymphs perform their last molt, after which the adult emerges. [18](https://www.johnnybutterflyseed.com/2023/07/07/holometabolous-insects-are-fabulous-insects/)

These insects are also called Exopterygota (from Latin exo- = “outside” + pteron = “wings”), because in these organisms the wings are progressively and visibly formed at the outside part of their body. [19](https://earthlife.net/insect-life-cycles-hemimetabolous-holometabolous/)

#### 3.2.2 Holometabolous metamorphosis

it’s considered the most radical metamorphosis in insects and also probably the most well known transformation by all of us. The most famous example is the one performed by lepidopterans (butterflies and moths); but there are also more insects that are holometabolous, such as coleopterans (beetles), hymenopterans (bees, wasps and ants) and dipterans (flies and mosquitoes). [20](https://australian.museum/learn/animals/insects/metamorphosis-a-remarkable-change/)

In the complex, complete or holometabolous metamorphosis, insects are born as larvae, that is, a premature stage that doesn’t resemble anatomically nor physiologically to the adult. In addition, they don’t share feed sources nor habitat, as it is the case of hemimetabolous organisms. As in hemimetabolous insects, these larvae go through successive molts until reaching the size enough to undergo the metamorphosis, when they perform their last molt. [21](https://www.insectlore.com/blogs/butterflies/the-mysterious-world-of-insect-metamorphosis?)

After their last larval stage, larvae enter in a stage of inactivity, moment they stop feeding and remain motionless. This stage is known as pupal stage (when they become a pupa or a chrysalis in butterflies). 

Once the transformation process ends, the organisms leave that motionless state and acquire their adult form that has wings and is mature. [22](https://bugunderglass.com/insect-metamorphosis-explained/?srsltid=AfmBOoo3HOdHuQIHVCQ1iWjN8CXeYZh3djIMjc8Zu55eiirfenieNdJE)

In contrast with hemimetabolous insects, the appearance of wings in holometabolous organisms takes place inside their body and become visible only at the end of the pupal stage. For this reason, they are also known as Endopterygota (from Latin endo-= “inside” + pteron=”wings”). [23](https://allyouneedisbiology.wordpress.com/tag/holometabolous-metamorphosis/)

### 3.3 Origin: the fossil record and natural seleciton

Insects are, as we discussed in previous articles, one of the animals with greater evolutionary success. Between 40%-60% of all insect species are holometabolous (complete metamorphosis), because of what we deduce that holometabolous metamorphosis was positively selected during the evolution of this group. In fact, fossil records suggest that this kind of metamorphosis appeared only once, so all holometabolous insects derive from the same ancestor.

According to these data, wingless insects or ancient Apterygota and early winged insects were ametabolous. Then, all winged insects started to develop some kind of hemimetabolous metamorphosis during the Carboniferous and the Permian (300 Ma). Finally, the first insects considered as holometabolous appeared during the Permian period (280 Ma).

The fact that different life stages of the same animal exploit different resources could prevent the intraespecífic competition (competition for resources between organisms of the same species). This fact would mean a great advantage for these organisms, so that holometabolous development, which is characterized for being divided in very different stages, could have been more successful than the hemimetabolous or the ametabolous. [24](https://forum.inaturalist.org/t/why-is-holometabolism-so-successful/17208)

Thus, we can say the main functional sense of metamorphosis could be to minimize the intraespecífic competition for resources. But there is still more: the more specialized are the different stages of an insect, the greater would be the chance to exploit more and better the resources. [25](https://www.natureoutside.com/holometabolism-transforming-one-animal-another-video/)

So, likewise the appearance of wings promoted the expansion and diversification of insects worldwide, the metamorphosis could have acted as a diversifying engine by increasing the capacity to exploit more and better resources. [26](https://pmc.ncbi.nlm.nih.gov/articles/PMC11420152/)

## 3.4. Inside the chrysalis

Inside the chrysalis, the caterpillar's body tissues break down and are reorganized into the structures of an adult butterfly, such as wings, antennae, and a proboscis. [27](https://www.wildlifewatch.org.uk/what-happens-inside-chrysalis)

Histolysis (Destruction): Enzymes are released that digest the caterpillar's body, turning it into a nutrient-rich soup. Most of the caterpillar's tissues are destroyed.

Histogenesis (Creation): Certain clusters of cells, called Imaginal Discs, survive the dissolving process. These discs function like blueprints; one disc is for an eye, another for a wing, another for a leg. They use the nutrient soup to build a completely new body from scratch. [28](https://www.floridamuseum.ufl.edu/discover-butterflies/faq/?hl=en-US#)

## 3.5 The Evolutionary "Why"

Why do they it this way and not others? The answer is Ecological Success.
Nature favors this method because it solves the biggest problem in nature: Competition.

A. No Competition with Parents
In animals that don't do this (like grasshoppers), the babies eat the same food as the adults. A baby grasshopper competes with its parents for grass.
 * The Butterfly Advantage: The caterpillar eats leaves. The butterfly drinks nectar. They live in the same world but never fight for the same dinner. This allows the population to be much larger.

B. Extreme Specialization
Because they have two distinct bodies, they can be perfect at two different things:
 * The Caterpillar: Is a specialized Eating Machine. It has no wings, no reproductive organs, and simple eyes. Its only job is to gather energy.
 * The Chrysalis/Butterfly: Is a specialized Sex & Travel Machine. It is streamlined, winged, and mobile. Its job is to find a mate and spread eggs to new areas.

## 3.6. Other types of metamorphosis

To understand why the chrysalis is special, we have to look at the "other ways" insects grow, which are evolutionarily older and often less efficient.
Type A: Ametabolous (No Metamorphosis)
 * Who: Silverfish, Springtails.
 * Process: The baby looks exactly like the adult, just smaller. It keeps molting and growing until it dies.
 * The Problem: They are inefficient. They cannot change their body plan to adapt to different seasonal needs.
Type B: Hemimetabolous (Incomplete Metamorphosis)
 * Who: Dragonflies, Grasshoppers, Cockroaches.
 * Process: They hatch as a "nymph." They look mostly like the adult but lack wings. They slowly grow wings on the outside of their body.
 * The Problem: The baby usually competes with the adult for food. Also, growing wings on the outside is awkward and makes them vulnerable to damage while they are growing.
Type C: Holometabolous (The Chrysalis Way)
 * Who: Butterflies, Beetles, Bees.
 * The Advantage: By developing wings inside the body (hidden in the imaginal discs) and then revealing them only after the chrysalis stage, they keep the delicate wings safe until they are fully formed.
Summary
The chrysalis is an evolutionary "time-out" that allows the animal to completely change its job description. It allows the child to be a glutton and the adult to be an explorer, ensuring that neither stops the other from surviving.

---

## Glossary 

**Epigenome**: The collection of all chemical modifications to an organism's DNA and associated proteins that affect gene expression without altering the underlying DNA sequence itself. These modifications act like a "dimmer switch" for genes and can be influenced by environment, diet, and stress. [29](https://www.cdc.gov/genomics-and-health/epigenetics/index.html) [30](https://www.liebertpub.com/doi/abs/10.1089/gen.43.09.11) [31](https://www.mdpi.com/1422-0067/25/8/4482) [32](https://www.savemyexams.com/a-level/biology/aqa/17/revision-notes/8-the-control-of-gene-expression-a-level-only/8-2-regulation-of-gene-expression-a-level-only/8-2-7-epigenetics/)

**Imago**: In biology, this term refers to the adult, sexually mature, and typically winged stage of an insect after its final metamorphosis (a butterfly emerging from a chrysalis). [33](https://academic.oup.com/nar/article/50/6/3203/6528909)

---

Ronni Ross  
2025
