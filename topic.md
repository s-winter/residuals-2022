---
layout: default
---

# Topic Area

With the increasing complexity of modern software systems, there
is a higher risk of residual bugs in their code bases, i.e., software
defects that escape quality assurance measures during
develo1pment and remain in the deployed systems. One facet of
the problem is the [richness and complexity of tasks imposed to
software](https://www.nasa.gov/pdf/418878main_FSWC_Final_Report.pdf), in particular in the context of emerging
autonomous systems (e.g., self-driving cars, robot manufacturing
systems, drones, etc.) where the software is expected to operate
under uncertain and non-deterministic conditions, for which the
state of the art solutions for software verification and testing still
fall short.

If triggered during execution, residual bugs can result in software
failures with severe consequences, depending on the application
area of the system. In order to cope with this problem, either the
amount of residual bugs needs to be decreased by better detection
and localization approaches or mechanisms to compensate for
their effects at run time need to be developed and evaluated
against residual bugs to demonstrate their efficacy. However,
residual bugs are rarely known and it is difficult to find a suitable
set of defects for software systems targeted in an evaluation, in
particular because there usually are further restrictions on the type
and complexity of those systems. To circumvent the problem of
finding enough previously reported residual bugs for a sound
evaluation, researchers often rely on software bug simulations to
create arbitrary numbers of bugs from correct code.
Such simulations need to resemble residual bug characteristics as
closely as possible to not threaten evaluation validity. From the
discussion of bug simulation approaches in the literature, we
observe that different bug models are used in different
communities and that the technical details of their simulations
differ.

# Workshop Contribution

The goal of the workshop is a thorough systematization of
knowledge (documenting the state of the art/practice and open
problems) in the field of residual bug simulations, which is
covered by researchers from different communities for similar
purposes, but with slightly differing requirements on constraints
on the bug models and simulation techniques used.
Accordingly, the seminar topics result from combinations along
three dimensions:  
1. state of the art/practice vs. open problems (i.e., beyond
the state of the art/practice),
2. residual bug models (i.e., what residual bugs are) vs.
bug simulation techniques (i.e., how residual bugs are
simulated), and
3. the three communities working on related problems, i.e.,
fault tolerance, software engineering, and security.

This results in four topics (combinations along the first two
dimensions) to be discussed within and across the communities.
State of the art/practice for residual bug models. A variety of
software bug models have been proposed in all three
communities, both based on empirical data or on intuitive notions
of what typical bug patterns are. Interestingly, both the intuitive
bug notions and the empirical data that constitute the basis for the
models differ across the three communities. The origin and the
rationale of these existing models has to be discussed both within
and across the communities. The different communities also use
different terminology and classification categories for specifying
bug models. A systematic investigation of the relationship
between the different terms and categories is desirable to facilitate
an exchange across the communities.

## Open problems related to residual bug models

Many existing
models are based on empirical data, which dates back several
decades. It is questionable, if the corresponding results are still
representative of modern software systems, in particular because
of the significant advances in program analyses and their impact
on software testing efficiency. Along a similar argument line, the
question arises how to keep bug models up to date as different
programming languages evolve to include mechanisms to avoid
certain bug types or efficient detection mechanisms enter
mainstream software engineering. Another important question is if
empirical data is suitable for residual bug models in the first place,
as it only resembles bugs that have been found, as opposed to
residual bugs, which have not been found as per their definition.
State of the art/practice for bug simulation techniques. A
major obstacle for the wide spread use of bug simulation
techniques is the overhead they entail. Mutation testing, for
instance, suffers from the need to execute all tests against all
mutants to assess test adequacy. In the fault tolerance area, fault
injections are mandated by modern safety standards (e.g., [ISO 26262](https://www.iso.org/standard/68383.html)),
but their application is explicitly limited to components of high
criticality to system safety because of the massive run time
overheads if applied in system-level tests. Therefore, any
implementations of bug simulation that reduce runtime overhead
or avoid superfluous/redundant executions are of great
importance. An assessment of the state of the art in this area is
expected to reveal optimization potentials that are to date only
exploited within an individual community, but could be of
relevance to the others as well.

## Open problems related to bug simulation techniques

As
indicated by the above description on the state of the art/practice,
the number of open problems likely outweighs the achieved
solutions, as the main application of bug simulation clearly lies in
the academic sector and only has limited influence on common
software engineering practice. The reason behind some of the
problems that hamper the widespread adoption of bug simulations
are theoretical, as is the case for equivalent mutant detection to
avoid the execution of “useless” mutants in mutation testing. It is
important to identify such hard bounds on efficiency gains that
better simulation techniques can obtain. At the same time, it is
equally important to identify to which degree these hard bounds
are relevant in practice or to which degree they can be
circumvented by well-designed heuristics (such as [Trivial
Compiler Equivalence](https://doi.org/10.1109/ICSE.2015.103) for equivalent mutant
detection).