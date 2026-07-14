## Accepted Papers

There were 13 papers submitted for peer-review to this workshop. Out of these, 10 papers were accepted for this volume - 5 as regular papers and 5 as short papers.


- **The TPTP Format for Interpretations**\
  Geoff Sutcliffe, Alexander Steen, Pascal Fontaine, Lydia Kondylidou

  Abstract: *This paper describes the (new) TPTP format for representing interpretations. The sources and properties of interpretations, which influenced the design of the format, are discusse. The format for Tarskian, Herbrand, and Kripke interpretations is described. Tools for verification and visualization of the interpretations are described.*
  
- **Efficient Multi-Scale Indexing with Dynamic IntMaps** (short paper)\
  Albert Eisfeld, Stephan Schulz

  Abstract: *Term and clause indexing are central technologies for efficient first-order theorem provers and similar reasoning systems. While there is a selection of basic technologies, most of them require an efficient mapping from function symbols (usually encoded as small integers) or other integer values to branches of a tree structure. With today’s wide variety of application problems, both the range of possible values and the cardinality of each individual map vary wildly. We present a data structure that is designed to be efficient in time and space at all scales and key distributions. Experiments show very good scalability and a modest improvement over the old, already quite refined data structure in E.*

- **A light-weight proof checker for TSTP refutations**\
  Melanie Taprogge, Happy Sariyanto, Alexander Steen

  Abstract: *The heterogeneity of proof outputs produced by different state-of-the-art automated theorem proving systems presents a considerable challenge for their efficient and uniform verification. In this paper, a proof checker called Nörgler is introduced that builds upon and extends the established approach pioneered by GDV. It supports checking propositional, (untyped and typed) first-order, and higher-order refutations represented in TSTP. For increasing flexibility and performance, Nörgler can parallelize proof checking tasks and incorporate model finders (for rejecting proofs). We evaluate the efficiency of Nörgler's design and implementation, and show that it outperforms GDV in terms of success rate and verification time on a benchmark drawn from the TSTP solution library.*

- **The TPTP Format for Clausal Connection Tableaux** (short paper)\
  Geoff Sutcliffe, Sean B. Holden, Mantas Baksys

  Abstract: *This paper describes the (new) TPTP format for writing clausal connection tableaux. The format builds on the existing infrastructure of the TPTP World, in particular the TPTP format for recording derivations. An ATP system that outputs tableaux in this format is described. Existing TPTP World tools for verifying and viewing derivations have been extended to verify and view tableaux in this format.*

- **Bridging the gap: A complete axiomatization of Gregorian date arithmetic and scheduling logic for automated theorem provers**\
  Adam Pease, Pantelimon Stanica

  Abstract: *First-Order Logic (FOL) theorem provers excel at symbolic reasoning but may struggle at tasks requiring complex integer arithmetic combined with irregular conditional rules. This limitation is most acute in temporal reasoning, where standard ontologies model time relationally rather than arithmetically. We present a novel “Universal System” that bridges this gap through a complete axiomatization of Gregorian calendar arithmetic implemented in the TPTP language. Our modular architecture comprises four interlocking engines: a Time Engine for minute-level rollovers, a Date Engine for Gregorian leap-year logic, a Scheduler Engine utilizing Zeller’s Congruence for weekday calculations, and a novel Integer Trap mechanism that forces arithmetic evaluation within the theorem prover. We demonstrate that this formalization enables the Vampire theorem prover to solve complex scheduling queries–such as finding “the 2nd Thursday of November 2025”–entirely within First-Order Logic, without recourse to external computational modules. Our evaluation on a comprehensive suite of 220 diverse temporal reasoning problems shows 100% accuracy, verified against Python’s datetime library for ±10,000 days (27.4 years)—the extent of Python’s BCE date support. The system demonstrates empirically O(1) constant-time performance (bounded by ≤ 30 major accelerator jumps) with coefficients of variation under 2% across six orders of magnitude, executing queries spanning ±1,000,000 days (2,738 years) in 456–473ms with identical performance characteristics. This includes leap year edge cases, complex scheduling constraints, and calculations extending from 714 BCE to 4762 CE.*

- **GenZ: A Generic Sequent Calculus Prover using the Zipper**\
  Xiaoshuang Yang, Malvin Gattinger, Marianna Girlando, Patrick Koopmann

  Abstract: *We introduce GenZ, a generic theorem prover for sequent calculi implemented in Haskell. Sequent calculus is a simple and versatile formalism, widely used to define proof systems for modal and non-classical logics. GenZ allows the user to specify a set of sequent rules, over which it performs proof search. This makes it possible to rapidly implement and test proof systems for a wide variety of logics, a useful feature for both research and teaching. To allow for efficient proof search, GenZ employs the zipper data structure. We illustrate our system by implementing eleven well-known sequent calculi for classical and intuitionistic propositional logics, as well as for several modal logics from the S5 cube, and evaluate it on formulas from the LWB and ILTP benchmark suites.*

- **Satisfiability for Probability Modalities**\
  Marcelo Finger, Tommaso Flaminio, Lluís Godo, Felip Manyà, Sandro Preto

  Abstract: *The fuzzy logical system FP(\L) extends \L ukasiewicz logic by replacing propositional variables with basic modal formulas of the form $P\phi$, expressing the fuzzy notion that a classical event $\phi$ is probable. In this work, we study the satisfiability problem for FP(\L) by presenting an algorithm and conducting an empirical evaluation over a controlled class of FP(\L)-satisfiability instances. Our experimental results reveal a clear phase transition behaviour and distinctive running-time patterns, shedding light on the computational properties of FP(\L)-satisfiability.*

- **Case Study: Saturations as Explicit Models in Equational Theories** (short paper)\
  Mikoláš Janota, Michael Rawson, Stephan Schulz

  Abstract: *Automated theorem provers (ATPs) can disprove conjectures by saturating a set of clauses, but the resulting saturated sets are opaque certificates. In the unit equational fragment, a saturated set can in fact be read as a convergent rewrite system defining an explicit, possibly infinite, model — but this is not widely known, even amongst frequent users of ATPs. Moreover, ATPs do not emit these explicit certificates for infinite (counter-)models. We present such a certificate construction in full, implement it in Vampire and E, and apply it to the recent Equational Theories Project [5], where hundreds of implications do not admit finite countermodels. The resulting rewrite systems can be checked for confluence and termination by existing certified tools, yielding trustworthy countermodels.*

- **Elixir meets TPTP: Bringing Automated Reasoning to the BEAM Ecosystem** (short paper)\
  Johannes Schuster, David Fuenmayor, Christoph Benzmüller

  Abstract: *Automated theorem provers (ATPs) are powerful tools for formal reasoning, yet integrating them into larger software systems remains cumbersome: existing interfaces are typically script-based, tightly coupled, or limited in working across multiple backends in a uniform way. We present AtpClient, an Elixir library that provides a unified, extensible interface to ATP services across four backends, SystemOnTPTP, StarExec, Isabelle, and locally installed provers, using TPTP standards. The library acts as a truth-grounding service for host applications: it exposes a consistent API that abstracts over differences in communication protocols, result formats, and termination semantics, and normalizes the verdict of each backend into a single result type. Built on the BEAM virtual machine, it benefits from robust process isolation, fault-tolerant result polling, and uniform cancellation, making it well-suited to multi-prover experimentation and portfolio solving. We describe the architecture, discuss key design decisions, and reflect on challenges encountered when bridging the gap between ATP services and a functional runtime. We further show how the library is consumed by two downstream tools built on it without backend-specific tinkering: a Livebook Smart Cell that turns it into an interactive TPTP editor, and a Model Context Protocol server that exposes the backends to LLM-based agents. AtpClient is open source and available on Hex, the Elixir package registry.*

- **Agent Hunt: Bounty Based Collaborative Autoformalization With LLM Agents** (short paper)\
  Chad Brown, Cezary Kaliszyk, Josef Urban

  Abstract: *We describe an experiment in large-scale autoformalization of algebraic topology in an Interactive Theorem Proving (ITP) environment, where the workload is distributed among multiple LLM-based coding agents. Rather than relying on static central planning, we implement a simulated bounty-based marketplace in which agents dynamically propose new lemmas (formal statements), attach bounties to them, and compete to discharge these proof obligations and claim the bounties. The agents interact directly with the interactive proof system: they can invoke tactics, inspect proof states and goals, analyze tactic successes and failures, and iteratively refine their proof scripts. In addition to constructing proofs, agents may introduce new formal definitions and intermediate lemmas to structure the development. All accepted proofs are ultimately checked and verified by the underlying proof assistant. This setting explores collaborative, decentralized proof search and theory building, and the use of market-inspired mechanisms to scale autoformalization in ITP.*
