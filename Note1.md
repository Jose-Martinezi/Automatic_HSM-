
GreenJ
.greenj
Online

AB — Today at 2:21 PM
download and extract this
Attachment file type: archive
proteus.zip
1.95 MB
GreenJ — Today at 3:46 PM
https://docs.google.com/document/d/14SbulAQLN07gH9qg_H_aQG5BYoBtYYU3OACYG-uTqWg/edit?usp=sharing
Google Docs: Sign-in
Access Google Docs with a personal Google account or Google Workspace account (for business use).
AB — Today at 3:50 PM
**[Given notes on the links:]{.underline}**

**[Hierarchical state machines (a.k.a. statecharts)]{.underline}** are
an advanced formalism for specifying state machines, which extends the
traditional automata theory in several ways.

Testing Word

Expand
hsmOutput.md
10 KB
AB — Today at 4:02 PM
git config --global user.name INSERT_NAME
git config --global user.email INSERT_EMMMMMAIL
﻿
AB
ab.
halfway decent

all 📠, no 🖨️
Jose Ocampo
**[Given notes on the links:]{.underline}**

**[Hierarchical state machines (a.k.a. statecharts)]{.underline}** are
an advanced formalism for specifying state machines, which extends the
traditional automata theory in several ways.

**[Hierarchical state machines]{.underline}** support state entry and
exit actions for states, which provide the means for guaranteed
initialization and cleanup, very much as constructors and destructors do
for classes. Entry actions are always executed starting with the
outermost state, which is analogous to class constructors executed from
the most general class. The exit actions, similar to destructors, are
always executed in exact reverse order. Entry and exit actions combined
with state nesting complicate the transition sequence.

**[State machines]{.underline}** can be an incredibly powerful
technique, but they require an **[infrastructure
(framework)]{.underline}** that at a minimum provides: a
run-to-completion (RTC) execution context for each state machine,
queuing of events, and event-based timing services. This is really the
pivotal point: Without an event-driven infrastructure, such as a
[Real-Time Embedded Framework](https://www.state-machine.com/rtef/),
state machines are like cars without an infrastructure of roads and gas
stations.

The relationship between an event-driven framework and state machines is
mutually synergistic. On one hand, the framework provides the thread
context and event queuing that the state machines need to process the
events in a run-to-completion fashion. On the other hand, state machines
provide the structure and clear design for the event-driven behavior
running inside the framework. State machines are also the most
constructive part of the design amenable to [modeling and automatic code
generation](https://www.state-machine.com/mbd/).

**[Zoom meeting notes:]{.underline}**

**[September 21, 2023:]{.underline}**

As said in the Zoom meeting on September 2, most of the code that is
used on very critical missions like satellites is going to be very
different from the things that you would see traditionally in code. The
first thing that he shows on the

**[September 28, 2023:]{.underline}**

**Differential Testing:** software testing technique that focuses on
identifying differences in the behavior or output of two or more
versions of a program or software component.

**[October 5, 2023 (Testing):]{.underline}**

Software Testing: There is "White Box Testing" and "Black Box Testing"

**Black Box:** Only have the interface of the software, but we do not
see it.

-   Has a function boundary.

-   Unit Boundary.

-   Executable boundary.

**White Box:** You have the whole code and you can see what is
happening.

The definition of **automated testing** is different depending on who
you ask.

**[In Industry:]{.underline}** Unit testing framework, tests are run
push-button style, tests are all written manually

**[In Academia:]{.underline}** "Automated test generation tests
themselves are automatically produced, automatically run.

**The Oracle Problem:** Knowing what test is supposed to make and what
is the correct output.

Some programmers will hardcode what the code is supposed to output, but
with automated testing, you don't know what the code is going to give
you nor do you know what the correct output is.

What kind of testing does Basil use?

Proteus are all unit tests and can be both Black and White Testing.

**[This was looked at for an example of testing:]{.underline}**

[Something to check out:]{.underline}

https://en.wikipedia.org/wiki/American_fuzzy_lop\_(fuzzer)#/media/File:AFL_Fuzz_Logo.gif

Thursday's 5-6, Fridays 4-5

**[October 6, 2023 (Testing):]{.underline}**

**Software Testing:** a systematic and organized process of evaluating
and verifying a software application or system to ensure that it behaves
as expected, meets specified requirements, and is free from defects,
errors, or bugs.

**Unit Testing:** This is more like function testing in your code to see
if the function that you are coding has no bugs in it.

**End-To-End Testing:** A testing technique that evaluates the
functionality and behavior of an entire software application from start
to finish to ensure that all its components and integrated systems work
correctly together.

**Automated Test Case:** A testing technique that uses automated tools
and scripts to perform tests on software applications or systems.
Instead of manually executing test cases, testers or test engineers
write scripts or use testing frameworks to automate the execution of
test cases, the comparison of actual results with expected results, and
the reporting of test outcomes.

**[October 12, 2023 (Status Update):]{.underline}**

**Step 1:** Code that will not be used, but can be used to test the
compiler. One thing that was suggested during the meeting was to
implement a calculator that takes strings and it prints out the results
of the string.

Java Calculator "1 + 2 \< 3"

False

**Step 2:** Write a test case generator (or test this any way you want)

"hfuakfhuiaudhj"

"(1 \< 2) \< 2"

**[October 14, 2023 (More Status Update):]{.underline}**

Just like before, they talk about making some code for the compiler to
run like a calculator.

Then we use this to test stuff.

-   Unit tests/code coverage/mutation testing.

-   Automated black-box test case generation.

-   Come up with strings that you can throw with this calculator.

**[October 19, 2023 (Automated Testing):]{.underline}**

**[Need help understanding this meeting!!!]{.underline}**

**[October 20, 2023 (More Automated Testing):]{.underline}**

**[Need help understanding this meeting!!!]{.underline}**

**[My own research:]{.underline}**

**[Any Questions:]{.underline}**

What is fuzzing in general and how does fussing help with HSM?

**[Presentation Notes (Try to make the presentation 15-20
mins):]{.underline}**

1.  Introduce the group members:

2.  What is your project? This is the first time class may be seeing
    > your project as a full idea?

    a.  Our group is currently studying a "Hierarchy State Machine"
        > (HSM).

        i.  A state machine, according to Professor Kyle Dewey, is a
            > type of finite state machine that is used to model and
            > control very complicated systems in software.

        ii. They are generally made up of States and Transitions.

3.  What tools have you set up or are planning to use? This can include
    > management/organizational tools:

    a.  Github will be used to share our files with one another.

    b.  Proteus: C-like language and is intended for aerospace software
        > such as space probes and satellites etc.

        i.  The code that is used in Proteus is very strange and not
            > like the traditional way programmers code.

        ii. It has built-in support for actors, hierarchical state
            > machines can be designed in it, and runtime monitors.

    c.  May have to use Swift coding at some point in the project.

4.  What research or learning has your team currently encountered or
    > accomplished on the project?

    a.  Most of the research and learning that has been accomplished
        > consists of watching Profs. Deweys Lecture on HSM in general,
        > testing techniques that we encounter on Proteus, looking at
        > what the code looks like so that we have a better
        > understanding of what to expect when programming in it.

    b.  There are some piece of information that I did not understand
        > such as certain terms that were used that I had to either
        > Google or ask Chat GPT for to understand their definitions.

5.  What decisions have you been faced with, how are you resolving those
    > decisions, what have you decided?

    a.  Currently the only decision that I have made so far is to
        > research with the information that is available to me at the
        > moment. I have yet to be put in a team yet due to some
        > complications. As so as I am put in a team we can start
        > collaborating with the information that we have gathered.

6.  What are your plans/timeline for the immediate and far future?

    a.  I am currently planning to be able to download the tools that I
        > need to be able to interact with the code that we are
        > currently visualizing from our studies.

    b.  Other than this and being put in a team that shares similar
        > scheduling with me, there is not much else that I have planned
        > currently. Some more communication with my project manager
        > might be necessary.

7.  What obstacles/Challenges are you grappling/expecting?

    a.  I am expecting to take in a lot of confusing information at once
        > and have to need time to process everything little by little.

    b.  The programming in this language is very different from what I
        > am used to so I may have to look at things from a different
        > angle.

I also still do not understand how the actual code for the past two Zoom
meetings work, so if someone could help me break down the code to a more
understandable level that would be most appreciated.
hsmOutput.md
10 KB
