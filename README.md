# Motivating Markov: In the Flow of Formal Language

Formal logic and language is powerful, and Markov chains exploit this power.

Meet Linda--a character within an experiment within a book within a blog post on said book. The post is What Ho!'s <a href="http://whatho.in/2013/plausibility-versus-probability/">"Plausibility and Probability"</a>, from which I paraphrase liberally. The book is economist Daniel Kahneman's <i>Thinking, Fast and Slow</i>; Dr. Kahneman and his colleagues designed "the Linda problem." Consider the following description:
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
By contrast, <i>System 2</i> (S2) applies logical rules to examine the soundness of drawn conclusions. One of Kahneman's assertions borne out from his studies is that System 1 is hyper-active and System 2 is extraordinarily lazy.

I'm now going to make explicit the analogy here between S2 and S1, and the logical criteria of <i>soundness</i> and <i>completeness</i>: S2 : S1 :: Soundness : Completeness.

In formal logic, soundness captures the move from theorems to axioms. Axioms--from <i>axíōma</i>, fittingness, from <i>*Ag-ty-o-</i>, "weighty"--are like premises. More precisely, logical axioms are statements that are taken to be true within the system of logic they define (e.g., that "A and B" implies "A" is true within a system of logic accepting of simplification as a rule of inference). Do all theorems reduce to axioms? Potentially, yes: in a logical system, there can be things that are "true." A default Pythonic logical system, e.g., adheres to Boolean logic. Such a system is said to be "sound."

Completeness, by contrast, is all about going from axioms to theorems. Theorems are like conclusions (rules, "theories"). Theorems are logical consequences of axioms and possibly other theorems. Can all axioms be expressed in theorems? No: what of the set containing all and only sets that do not contain themselves? Gödel: completeness of a system is impossible.

Gödel's notion of systematic incompletness seems to relate to what we know about natural languages. “Natural languages are the languages people speak, such as English, Spanish, and French. They were not designed by people (although people try to impose some order on them); they evolved naturally” (Allen Downey, <a href="http://interactivepython.org/courselib/static/thinkcspy/GeneralIntro/FormalandNaturalLanguages.html"><i>How to Think Like a Computer Scientist</i></a>). Also see Quine's "barber paradox" for a Gödelian take-down of natural language capabilities in re logic. 

By contrast, a formal language grammar (when the context is not given, often called a formal grammar for clarity) is a set of production rules for strings in a formal language. The rules describe how to form strings from the language's alphabet that are valid according to the language's syntax. As Downey notes,
<blockquote>
“Formal languages are languages that are designed by people for specific applications. 

“Programming languages are formal languages that have been designed to express computations. 

“Formal languages tend to have strict rules about syntax, and syntax rules come in two flavors, pertaining to tokens and structure. 

1. “Tokens are the basic elements of the language, such as words, numbers, and chemical elements. One of the problems with 3+ = 3$6 is that $ is not a legal token in mathematics (at least as far as I know). Similarly, 2Zz is not legal because there is no element with the abbreviation Zz. 

2. “The second type of syntax rule pertains to the structure of a statement; that is, the way the tokens are arranged. The statement 3+ = 3 is illegal because even though + and = are legal tokens, you can’t have one right after the other. Similarly, in a chemical formula the subscript comes after the element name, not before.” (e.g. H2O) (Downey)
</blockquote>

This latter type of syntax rule recalls Markov memorylessness: the underlying assumption of the Markov property implies that the properties of random variables related to the future depend only on relevant information about the current time, not on information from further in the past.

Now that we’ve discussed S1/S2 in terms of completeness vs. soundness let’s bring the analogy back to include plausibility vs. probability, and extend it somewhat: 
<blockquote>
S1 : S2 <br />:: Completeness : Soundness <br />:: Plausibility : Probability <br />:: Control : Power <br />:: Natural Language : Formal Language.
</blockquote>

Properties specific to formal languages exercise power (versus control). Consider the lack of control or uncertainty inherent in Markov memorylessness. Freeing, no?

As is documented step by step in `markov.ipynb` a Markov text generator consists of (1) getting an initial state, and (2) iteratively getting subsequent states based on (transformation from) previous states. One might call the results incomplete or fragmentary, and certainly implausible: natural language just doesn't cohere like that. Yet, there <i>does</i> seem to be a formal sense of coherence to the results of a Markov transformation of text, a soundness, even the power to translate a sentiment (see the <a href="http://what-would-i-say.com/">"What Would I Say?"</a> generator). The results are hilarious and uncanny both.

In other words, Markov chains exemplify the power of formal language.
