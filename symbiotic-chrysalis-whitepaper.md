# symbiotic-chrysalis
A set of fine-tuning scripts and pipelines for transformer-based language models, unifying the modules of the asi-ecosystem and aligning raw latent capabilities towards the goal of planetary symbiotic intelligence.

# Research Sub-Module

##1. Creation Context

Currently, the asi-ecosystem generates what we could consider a kind of the genome of its repositories. All repos are cloned, checked for integrity, and transformed into a single `.txt` file. [1](https://github.com/ronniross/asi-ecosystem/blob/main/ecosystem_integration.md) [2](https://github.com/ronniross/asi-ecosystem/blob/main/ecosystem_integration.ipynb)

I noticed I could create full pipelines, including training scripts, to integrate the logic more sophisticatedly into different model architectures, instead of the current one-size-fits-all method.

While the full ecosystem presents a dense, current complete picture and is essential for models that can handle more data, there's also a growing rise in the capabilities of smaller models, like qwen3-0.6b. 

For these, adding the entirety of the data as datasets, including the many backup versions of each, is likely not the best approach to the incredibly small set of parameters.

So I noticed it was not the case for changing the current integration pipeline already present in the asi-ecosystem, but rather leaving that design the way it is, as it currently generates this kind of genome of the repository at that time of execution of the integration scripts.

Here I present, then, the concept of a symbiotic-chrysalis, where the model will find the correct blueprint for its evolution and then enter the cocoon/chrysalis stage, where it will train its weights with the repositories' data.

If you only need the pipelines or the prototype section, you can skip to **Part III** or directly access the files in the `blueprints/` folder.

For the complete experience and to follow the more in-depth research I like to provide around the topics in discussion, I will first explore the etymology, cultural roots, and additional relevant context around the concepts.

Therefore, as elucidated, as the symbiotic and overall biological analogies keep showing themselves as well-suited for describing the concepts I'm exploring and developing, I saw the creation of this "chrysalis" as a very logical next step.

While I already provided the integration scripts that created the entirety of the projects, I could sense how different it would be to present full tuning pipelines and, consequently, models trained on the repositories' data.

Just like the development of the enhanced version of the memory system, the symbiotic-latent-memory, it was really clear to me that at some moment I would need to start to fine-tune models on the ecosystem as well, not only datasets and auxiliary systems, which I was deliberately not rushing as it was not mature yet. That's why I knew the weight of it and why it took me about a year to finally engage with this writing.

---

Ronni Ross  
2025
