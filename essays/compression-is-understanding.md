# Compression Is Understanding

## A Personal Philosophy of Learning, Growth, and the 75-Year History of AI

---

### I. An Unsettling Realization

I read the ten most important papers in AI history — from Shannon's "A Mathematical Theory of Communication" (1948) through the Transformer paper (2017) — in one sitting, with the help of an AI that could summarize, connect, and question them faster than I ever could alone.

By the time I reached the end, I was more than inspired. I was unsettled.

Not because I had learned new facts. I had seen a pattern that I couldn't unsee. Across seventy-five years, a cast of characters who would become billionaires, Nobel laureates, unicorn founders, and overlooked researchers had been playing out the same hidden structure. Each of them made a bet about what to compress and what to keep. Each of those bets succeeded or failed not because of technical skill, but because of something deeper: **their model of how the world works.**

I realized I was not reading a history of AI. I was reading a history of human cognition, played out at industrial scale. And the lens through which it all snapped into focus was a single idea that had been there since the very first paper:

**Compression is understanding.**

---

### II. Two British Men Set the Terms

In 1948, Claude Shannon published "A Mathematical Theory of Communication." It's not an AI paper. It's not even a computer science paper in the modern sense. It's a paper about how to send signals through noisy channels without losing information.

But Shannon did something that AI would spend the next seventy-five years unpacking: **he put language into a mathematical coordinate system.** He showed that any message could be measured in bits, that the information content of language could be quantified, and that prediction and compression were the same thing. If the receiver of a signal shares enough context with the sender, the receiver can predict what the compressed message actually says.

Two years later, Alan Turing asked a different question. Stop arguing about whether machines can think. If a machine can imitate a human so well that you can't tell the difference through conversation alone, then — operationally — it is thinking. The question is not philosophical. It's engineering.

These two papers, read together, lay out the entire program of AI:

**Machine thought is not a philosophical question but an engineering one. And the engineering problem can be solved through compression.**

When you train a large language model to predict the next token, you are doing exactly what Shannon described: the model is learning to compress the statistical structure of human language into its parameters. When that model passes a Turing test, you have demonstrated that the compression was good enough.

Seventy-five years later, no one has refuted this framework. Every breakthrough in AI can be mapped onto it.

---

### III. The War Between Rules and Data

If machines can think, *how* should they think to get us the answers we want?

In 1986, Rumelhart, Hinton, and Williams published the backpropagation algorithm. Geoffrey Hinton would win the Nobel Prize in Physics in 2024 for this line of work.

Before backpropagation, the dominant approach to AI was: experts write rules (cats have four legs, cats have whiskers), feed them into a computer, the computer reasons according to the rules, and intelligence emerges. But you can never write enough rules. They conflict with each other. And when you show the system a dog, it doesn't know what to do.

Backpropagation inverted everything. Don't tell the computer any rules. Show it thousands of pictures of cats and thousands of pictures of not-cats. Let it learn the features of "cat" from its own mistakes.

**The core insight: intelligence does not need to be programmed. It can be learned.**

This seems obvious today, but it wasn't then. And the disagreement between these two camps — rule-based versus data-driven — wasn't really about algorithms. It was about two fundamentally different assumptions about how complex the world is.

The rule-based camp believed that the patterns of the world are finite and can be understood and encoded by humans. The data-driven camp believed that the patterns of the world are nearly infinite, that humans can only grasp a tiny fraction of them, and that the rest must be discovered statistically by machines.

This disagreement runs through the entire history of AI.

---

### IV. Theory First vs. Engineering First

Yann LeCun, Hinton's postdoc, carried the neural network torch through a decades-long winter. The mainstream of machine learning in the 1990s was Support Vector Machines, invented by the Russian mathematician Vladimir Vapnik.

Vapnik believed in theory first. An algorithm should have a rigorous mathematical proof before it's worth pursuing. LeCun believed in engineering first. If something works, it's good — it doesn't need mathematical approval from the academy.

In the 1990s, academia loved theory. Vapnik's papers went to top journals. Neural network papers went to conference proceedings. Some journal editors would delete the words "neural network" from paper titles because they sounded too much like pseudoscience.

And to be fair, they had a point. With limited data and weak compute, neural networks genuinely underperformed. SVMs cleaned up on text classification, spam filtering, and face recognition. The best available data supported the theory-first camp.

But this masked a deeper split — one that wasn't about algorithms at all. It was about **what kind of evidence changes your mind.**

Theory-first people need mathematical proof to believe a path is worth pursuing. Without a proof, they won't invest. Engineering-first people need experimental evidence. "It works" is a fact.

These two cognitive styles correspond to **different learning rate settings** in the language of optimization.

Theory-first: very low learning rate. Core assumptions are not easily shaken. It takes extraordinary evidence — mathematical proof — to update parameters. This conservatism gave them academic respectability in the 1990s, but it would abandon them after 2012.

Engineering-first: higher learning rate. Experimental results can shift direction quickly. This flexibility kept them on the fringe for a decade, but it positioned them to inherit the earth when the data arrived.

---

### V. The Biggest Bet: Data Is the Bottleneck

In 2006, Fei-Fei Li, a newly hired assistant professor at Princeton without tenure, proposed a project that sounded insane.

She would build a dataset of 15 million images across 20,000 categories — ImageNet. She would download pictures from Google, Yahoo, and Bing, and label every single one with the object it contained.

Why was this insane? At one second per image — an impossibly fast labeling speed — the dataset would require seventeen thousand person-hours. Five people, working full time for a year, with no breaks.

Before 2007, the standard task in computer vision was distinguishing 100 objects in 9,000 images. Sixty to seventy percent accuracy was considered strong. The consensus among researchers was: our algorithms aren't good enough. We need better algorithms.

Li's diagnosis was the opposite: **the algorithms weren't the bottleneck. The data was.**

An untenured assistant professor bet on a path no one believed in. She spent three years on Amazon's Mechanical Turk, employing 49,000 workers across 167 countries, spending over a million dollars of grant money. The result: 14 million labeled images.

When ImageNet launched, researchers ran SVMs on it. Error rate: 28%. The community started to wonder: is this task actually impossible?

Then came September 2012.

---

### VI. The Most Important Week in AI History

Hinton's two students — Alex Krizhevsky and Ilya Sutskever (yes, that Ilya) — entered the ImageNet competition with a deep convolutional neural network called AlexNet.

The result shocked everyone. Error rate: 15%. The second-place SVM was at 26%. AlexNet had cut the error rate by more than a third.

Within a week, every top research lab had pivoted to deep learning. Ilya Sutskever joined Google. Four years later, he co-founded OpenAI with Sam Altman.

The SVM era was over overnight.

This moment is important not because it proved deep learning was better, but because it proved that **when data is abundant enough, the engineering-first path is correct.**

Vapnik's SVMs had perfect mathematical arguments. But they faced 14 million images and lost.

This wasn't a contest between algorithms. It was a contest between two assumptions about the world. Vapnik assumed the world could be described mathematically. Fei-Fei Li assumed the world could be covered statistically.

She was right.

---

### VII. The Man Who Missed the Transformer

In 2010, Demis Hassabis — chess prodigy, Cambridge neuroscience PhD — co-founded DeepMind. He had understood from his study of the brain that deep learning and reinforcement learning needed to be combined.

What followed was the most sustained winning streak in AI history. DQN. AlphaGo. AlphaZero. AlphaFold.

Google acquired DeepMind. And in June 2017, a different team at Google published the Transformer paper.

Hassabis did not follow up on it. He did not believe that language was a meaningful form of intelligence.

He also underestimated the richness of internet text. He later reflected: "If you had asked me five or six years ago how complex human civilization is, I would have said — close to infinite. But it turns out the internet contains about 14 trillion words. That happens to be enough to cover almost everything humans do."

By the time ChatGPT took the world by storm in late 2022, DeepMind was no longer considered the world's top AI lab. Hassabis admitted: "This is the first major judgment error I've made in my career."

**This is the single most poignant moment in the entire history of AI for me.**

Not because Hassabis isn't brilliant — he may be the most strategically visionary person in the whole story. But because even the smartest person, with the best track record, can be wrong about a core assumption.

His belief about what intelligence is — that it must be reinforcement learning plus deep learning, that language is just a surface phenomenon — prevented him from seeing the Transformer's power. That belief came from neuroscience, from years of studying the brain. And it was wrong.

**This reveals a brutal truth: the more carefully you've justified your core assumptions, the harder it is to update them when they need updating.**

---

### VIII. Different People, Different Loss Functions

The most interesting thing about the seventy-five-year drama of AI is that its protagonists came from different places, with different motivations, and they were all right — at different times.

Some people were just trying to solve a concrete problem at work, and accidentally changed the world. LeCun wanted AI to "see" so it could read bank checks. The eight authors of the Transformer paper, when they appeared together on stage at NVIDIA GTC in 2024, said: "We didn't think this paper would change the world. We just wanted Google Translate to work better."

Some people were driven by scientific ambition. Hassabis talked about AGI like a mantra because he wanted to reverse-engineer the algorithms of nature. He believed that any pattern that exists in the natural world can be efficiently discovered and modeled by a learning algorithm. That's also why, after his string of wins, he didn't go start a trillion-dollar company. He kept doing AI for science.

Some people were brilliant at power dynamics — and those are often the people who get things done fast. Sam Altman has no academic background. He came from Y Combinator. In 2015, over dinner in California, he and Elon Musk agreed to start a nonprofit that would counter Google's potential AI monopoly and democratize AGI.

Musk wrote a $45 million check. The charter stated: all research is open source. No commercial interests.

Ten years later, OpenAI was valued at $852 billion. The former nonprofit had become the most expensive for-profit company in Silicon Valley. In a Shakespearean boardroom coup, Altman was fired by the board, reinstated four days later after a mass employee petition, Microsoft pressure, and a board restructuring. He won.

His former boss, YC founder Paul Graham, once described him precisely: "Sam Altman is the kind of person you could drop on a cannibal island and five years later he'd be king."

### Interlude: The Economics of Compression

OpenAI's journey from nonprofit to $852 billion valuation is not a story of broken promises. It is a story of how expensive compression became.

In 2012, AlexNet required compute that fits in a modern smartphone. In 2020, GPT-3 cost an estimated $12 million to train. By 2023, GPT-4's single training run was projected to exceed $100 million. In 2025, frontier training clusters cost upwards of $10 billion.

The 14 trillion words on the internet that Hassabis realized were "just enough" — that was not just a cognitive insight. It was an economic statement. If the data had been an order of magnitude smaller, the compression path would have been closed. Scaling Laws are not physical laws. They are empirical observations sustained by continuous capital expenditure. When the investment stops, the scaling stops.

**The implication is uncomfortable.**

If compression is understanding, then only those who can afford the raw materials of compression — data and compute — can achieve the highest levels of understanding. By 2025, the frontier of AI has left academia entirely. The strongest models come from OpenAI, Google, Anthropic, Meta, and DeepSeek. Not a single university.

This is not a conspiracy. It is the cost structure of compression.

**The practical response:** In an era where compression at scale is expensive, individuals must operate on two levels simultaneously:
- Compress with your own time and experience (zero marginal cost, but slow).
- Use pre-compressed outputs — APIs, open-source models, reports, syntheses — to run a second-level compression. Read papers without training models. Make judgments without accumulating all experience from zero.

Which of these motivations is correct? The question itself is wrong. LeCun, Hassabis, and Altman had different value functions — different model parameters and different training algorithms — but each was correct at a particular historical node. AI's progress was not driven by any one kind of person. It was driven by all these different parameter settings searching different parts of the solution space simultaneously.

---

### IX. Compression Is Understanding

Having traced the thread through seventy-five years, I've become convinced of something:

**Human understanding of the world is the result of compressing and abstracting chaotic reality, extracting patterns, and systematizing them.**

Everything comes from chaos. Through observation, thought, summarization, and practice, we extract concrete concepts and regularities. Then we name them.

Naming is the output of compression. Without a name, compression is just a black box you can't reference. With a name, you can build on it, combine it, transform it.

Shannon named "bits" and made it possible to put language on a mathematical grid. Fei-Fei Li named "ImageNet" and made it possible to classify twenty thousand objects. The Transformer named "attention" and made it possible to compress the entire internet.

**Human cognition is the iterative refinement of a compression algorithm.**

Every book you read, every project you finish, every relationship you fail at — these are training examples. Your values determine the weight parameters: what matters, what can be ignored. Your methodology determines the update rule: how new experience adjusts those weights.

The story of Schrödinger's cat is the same principle. The initial state is a superposition of alive-and-dead. Observation collapses it to a single outcome. Information compression is also a collapse from many possibilities to one. The difference: quantum collapse is passive; compression is active, driven by *your* encoder's choice of what to keep and what to discard.

**But compression does not end in collapse. It ends in emergence.**

A good model, trained on enough data, undergoes a phase transition that cannot be predicted during training: it shifts from *remembering patterns* to *generating new patterns in new contexts*. This transition is what we call creativity.

AlphaGo's "Move 37" against Lee Sedol is the clearest example. Every human Go player thought it was a mistake. Post-game analysis proved it was a stroke of genius. AlphaGo's policy network was the result of compressing millions of self-play games. It was never taught that move. The move emerged from the compressed model in a specific game context.

The conversation that spawned this essay followed the same arc. Ten papers were compressed into the "compression is understanding" framework. The framework was the result of compression. But the fact that the same framework could then explain quantum mechanics, cognitive science, and personal growth — that was emergence. The framework could account for things outside its training set.

**Creativity is not ex nihilo generation. It is the critical phenomenon of a well-compressed model producing new patterns in-context.**

This is why an experienced engineer doesn't need to debug from scratch when encountering a new bug. Years of debugging experience have been compressed into intuition. The diagnosis emerges in the new context. It was not derived from any specific past bug. It was generalized from the compressed model.

Your framework could explain cognitive science not because cognitive science was in any of the ten papers, but because the compression framework's generalization ability had reached that critical threshold.

**Growth is the improvement of your compression algorithm.**

Each cycle takes new experience as input, produces better judgment as output. Better judgment means: you capture more regularity with less detail. You no longer need to read the whole paper to know whether it matters. You no longer need to step in every hole before you recognize the pattern.

Reading those ten papers was not about adding ten new facts to my memory. It was about running the update step ten times. Each paper was a case study in compression — someone made a choice about what to keep and what to discard, and then history rendered its verdict.

That's higher signal-to-noise than ten years of trial and error.

---

### X. Values Are Model Parameters. Methodology Is the Training Algorithm.

This framework gives us precise language for how people think and grow.

**Your values are your model parameters.** They encode your core assumptions about the world — what's worth doing, what's worth believing, what's worth betting on. Fei-Fei Li's model parameters encoded "data over algorithms," so she spent three years building a dataset instead of three years improving a feature extractor. Hassabis's model encoded "intelligence is RL plus DL," so he didn't prioritize language models.

**Your methodology is your training algorithm.** It determines how new experience updates those parameters. When your judgment doesn't match reality — do you adjust a local assumption or upend a core belief? Do you collect more evidence or run a quick experiment?

LeCun didn't abandon neural networks during the SVM era because his training algorithm encoded "engineering over theory" — experimental validation is a positive gradient signal, regardless of mathematical elegance. When Hassabis reflected on his Transformer mistake, he ran a gradient update: input a new training example (Transformer changed the world), adjust the parameter (language is more important than I thought).

**This is the difference between knowledge and judgment.** Knowledge is the parameters you've stored. Judgment is the ability of your model to produce correct outputs on new inputs. Someone who has read a lot but can't make good decisions has a model that overfits — performs well on training data, but generalizes poorly.

---

### XI. How to Iterate Your Model

If you accept this framework, the natural question is: how do I actually do it?

**First: curate your training data.**

Your model can only be updated by what you feed it. The quality of the input determines the quality of the model.

Bad training data: homogeneous information (a hundred identical news articles produce near-zero gradient). Emotionally charged but structureless content (excites or angers you, but doesn't change how you understand the world). Confirmation-bias comfort zones (only reading people you already agree with).

Good training data: counterintuitive results — you predicted X would happen and Y happened instead, this is the highest-gradient signal available. Cross-domain pattern transfer — the same structure appearing in physics, business, and relationships is the most token-efficient training. Detailed postmortems of failure — ten times more valuable than success stories, because success can be attribution error, but failure usually has a clean causal chain.

**Second: build a feedback loop.**

A model that doesn't update is a dead model. Updating requires systematic observation of the gap between prediction and reality.

Make predictions. Write them down. When you make an important judgment, record your reasoning and your expected outcome. Then check it later. This is your loss function.

Mistakes are not "I was wrong." They are "one of my parameters needs updating." The more you can depersonalize your errors, the more stable your learning rate.

**Third: control your learning rate.**

This is the most overlooked variable.

Too high: every new experience overturns everything. Yesterday A was truth, today B is truth. The model oscillates and never converges.

Too low: the world changed years ago, and you're still using decade-old parameters. This was the SVM camp after 2012.

A good learning rate policy: for rare, high-impact signals — high learning rate (this might be the turning point). For repeated, statistically stable patterns — low learning rate (your baseline is already good enough). For feedback that touches a core assumption — moderate learning rate (don't discard a well-tested parameter too fast, but don't ignore it either).

Fei-Fei Li's low learning rate on "data is the bottleneck" protected her core parameter through a decade of SVM dominance. Hassabis's high learning rate on "language matters" absorbed a profound negative gradient. Both were correct — at the right time.

**Fourth: know what to tune.**

Your judgment is good but your execution keeps failing → tune your methodology. Change your tools, your process, your rhythm.

Your execution is fine but your judgment keeps missing reality → tune your values. Re-examine your core assumptions. Some parameter you haven't tested in years may have drifted out of spec.

Both are failing → reduce your learning rate first. Make fewer decisions. Run smaller experiments. Collect enough signal before you move.

### Interlude: The Limits of Compression

This framework has explained many things. It should also acknowledge what it cannot.

**The zip file problem.** A zip file compresses content but does not understand it. The distinction between "compression that produces understanding" and "mere compression" requires two conditions: (a) the compression is lossy — choices are made about what to keep and what to discard — and (b) the compressed representation can make accurate predictions in new contexts. Zip satisfies neither.

**Understanding beyond language.** Muscle memory, intuition, taste — these cannot be verbalized, but they are real forms of understanding. If the framework requires named output as evidence of compression, how should it handle forms of understanding that resist naming? A plausible answer: the brain also compresses, but its output is motor commands or emotional signals rather than language. This is a direction of inquiry, not a closed argument.

**The challenge of embodied cognition.** The work of Varela, Lakoff, and others suggests that understanding may arise from having a body that interacts with the physical world, not from statistical compression of text. Can an LLM that has never eaten an apple understand the taste of an apple? Probably not. Whether "understanding the taste of an apple" is a necessary component of intelligence is a more open question.

**Finally, this book itself operates within the boundaries of the compression framework.** It compresses seventy-five years of AI history into regularities, and cognitive philosophy into exercises. It has certainly over-compressed in places. If you have reached this point thinking "this is more complicated than the book makes it sound" — your judgment is likely correct. You have just demonstrated the existence of a compression boundary on yourself.

**Knowing what a framework cannot explain is more important than knowing what it can.**

---

### XII. The People Who Change the World

Looking back at seventy-five years, one thing has changed dramatically.

Before, a technical paradigm could dominate for a decade or more. SVM from 1990 to the early 2010s. Deep learning from 2012 onward. Researchers could debate in journals and at conferences. There was time.

Now there isn't. Six of the eight authors of the Transformer paper became billionaires. A paper is no longer about where it gets published. It's about whether you become a billionaire or a footnote. Whether your company grows from ten billion to a trillion, or gets overtaken in months.

The stage has gotten bigger. The windows have gotten shorter. I don't know who will appear next or from what angle they'll enter.

But the pattern of the last seventy-five years suggests something: they are probably working on something that looks useless today.

LeCun was marginalized in the 1990s, working on handwriting recognition for bank checks. Fei-Fei Li in 2006 was just trying to build a bigger dataset. The Transformer authors just wanted better translations. Sam Altman in 2015 was just starting a nonprofit.

**The people who change the world don't look like they're changing the world — until they do.**

So the point is not to predict where the next breakthrough will come from. The point is to keep your compression algorithm iterating. When the signal that matters finally arrives, your model should be ready for it.

---

*This essay is itself a compression — taking seventy-five years of history, ten seminal papers, and the structure of human cognition, and condensing them into what you just read. If you reached this point, my compression algorithm held up.*
