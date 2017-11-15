# Motivating Markov: In the Flow of Formal Language

Formal logic and language is powerful, and Markov chains exploit this power.

Meet Linda--a character within an experiment within a book within a blog post on said book. The post is What Ho!'s "Plausibility and Probability" (http://whatho.in/2013/plausibility-versus-probability/), from which I paraphrase liberally. The book is economist Daniel Kahneman's <i>Thinking, Fast and Slow</i>; Dr. Kahneman and his colleagues designed "the Linda problem." Consider the following description:
<blockquote>
Linda is thirty one years old, single, outspoken and very bright. She majored in English Literature. As a student, she was deeply concerned with issues of discrimination and social justice, and also participated in anti-nuclear demonstrations.
</blockquote>
After reading Linda’s profile, respondents in Kahneman et al.'s studies were asked "which of the following is a more probable alternative?"
<blockquote>
(A) Linda is a bank teller.<br />
(B) Linda is a bank teller and is active in the feminist movement.
</blockquote>

The wording is tricky. How about if I posed two versions of the question:
<blockquote>
Which of the following is a more <i>probable</i> alternative?<br />
(A) Linda is a bank teller.<br />
(B) Linda is a bank teller and is active in the feminist movement.
</blockquote>
<blockquote>
Which of the following is a more <i>plausible</i> alternative?<br />
(A) Linda is a bank teller.<br />
(B) Linda is a bank teller and is active in the feminist movement.
</blockquote>

In one survey, 89% of undergraduate students at top ranked American universities picked (B). Similarly, 85% of doctoral students at Stanford Business School chose (B). In fact, these respondents chose the more plausible but less probable event over the less plausible but more probable one. In Kahneman's language, they were predominantly relying on "S1 thinking."

Kahneman takes thinking to be a product of two systems. <i>System 1</i> (S1), which processes data, reflexively forms patterns and draws conclusions. As What Ho! writes,
<blockquote>
What (the system 1 of) our mind does is to jump to the most plausible or coherent conclusion. It does not consider the likelihood of the conclusion. The mind substitutes likelihood with representative-ness of the event. This is how we make errors in judgment that can have far reaching impact on society at large.
</blockquote>
By contrast, <i>System 2</i> (S2) applies logical rules to examine the soundness of drawn conclusions. One of Kahneman's assertions borne out from his studies is that System 1 is hyper-active and System 2 is extraordinarily lazy.<br />

I'm now going to make explicit the analogy here between S2 and S1, and the logical criteria of <i>soundness</i> and <i>completeness</i>. (S2 : S1 :: Soundness : Completeness.)

In formal logic, soundness captures the move from theorems to axioms. Axioms--from <i>axíōma</i>, fittingness, from <i>*Ag-ty-o-</i>, "weighty"--are like premises. More precisely, logical axioms are statements that are taken to be true within the system of logic they define (e.g., that "A and B" implies "A" is true within a system of logic accepting of simplification as a rule of inference). Do all theorems reduce to axioms? Potentially, yes: in a logical system, there can be things that are "true." A default Pythonic logical system, e.g., adheres to Boolean logic. Such a system is said to be "sound."

Completeness, by contrast, is all about going from axioms to theorems. Theorems are like conclusions (rules, "theories"). Theorems are logical consequences of axioms and possibly other theorems. Can all axioms be expressed in theorems? No: what of the set containing all and only sets that do not contain themselves? Gödel: sheer completeness of a system is impossible.

Now that we’ve discussed S1/S2 in terms of completeness vs. soundness let’s bring the analogy back to include plausibility vs. probability, and extend it somewhat: S2 : S1 :: Soundness : Completeness :: Plausibility : Probability :: Control : Power :: natural language :: formal language.

Properties specific to formal languages exercise power (versus control). Consider Markov memorylessness: the underlying assumption of the Markov property implies that the properties of random variables related to the future depend only on relevant information about the current time, not on information from further in the past. Freeing, no?

As is documented step by step in `markov.ipynb` a Markov generator consists of (1) getting an initial state, and (2) iteratively getting subsequent states based on (transformation from) previous states. Such a transformation need not adhere to any particular logical system beyond what gets defined (or left unturned) in the function itself. The results, I find, are both hilarious and uncanny.

In other words, Markov chains exemplify the power of formal language.
