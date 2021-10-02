# What is Scenario Hunting? 
Scenario Hunting is a process of switching from modeling artifacts to test code. The process consists of a set of steps that continually puts flesh on the model to the point that the test cases can be automatically generated from the model.

The test code generation is as cheap as a spike but as high quality as production, because the tests are derived from design, and speak the language of the domain. You achieve higher quality with lower cost.


# The problem with traditional approaches
- Yoyo problem
- Mistranslation of model to the code
- Code divergence from the design
- Long feedback loop (big design upfront)
- Drastic cost of jumping into implementation instead of smoothly drilling down to get the feedback about the feasibility of the proposed model
- Low level concerns influence high level concerns. Mixing  the complexity of high level requirements with the complexity of technical environment and implementation ends up less focus on both eg: solving/considering compile errors before discovering the higher level abstract requirements. 
- Boring, and resource intensive onboarding
- Lots of unplanned meetings, otherwise guess work during implementation of implicit concepts
- Stip test automation learning curve
- The gap between requirement concerns and technical concerns
See how they happen (TBD)

# Why Scenario Hunting? 

How does scenario hunting elevate the problems of traditional approaches?
By asking to reverse narrate the scenarios and to clarify the causality behind the elements from the model that participate in the scenario at each step, to identify the inconsistencies in the model and discover the missing elements before switching to code. You avoid paying for the drastic cost of discovering them at the implementation phase, and separate the requirements' concerns with the technological concerns. And finally generating the test code based on formal code templates as a scenario becomes successfully extracted from the model, and since there is a one to one relationship between the test steps and design elements, the feedback about the impact of the model on the lower level implementation and the feasibility of the implementation can be tracked easily, and the corresponding adjustments can be applied to the bigger picture model before paying for the cost of implementing more scenarios. 

At requirements engineering and design phase, brute forcing the causality of the implicit alternative paths after discovering the happy path is quick and easy when it's not combined with the complexity of understanding and dealing with the code. As the result it makes the requirements explicit which avoids unplanned meetings and guess work on the behalf of the iteration. So it improves estimation accuracy, because of conjecture reduction.

Scenario Hunting has a familiar, simple abstract language and tool set.

The power of abstraction and automation make it easy for the new developers to understand how the model is being translated into working code. They Hunt a Scenario, select a template, generate the code, so see the test automation policies and coding standards the team adhere to, in the generated code. The less time they need senior developers to guide them the less cost.

# Isn't it waterfall?
Doesn't Scenario Hunting require big design upfront? 

Scenario Hunting not only doesn't require the model of the whole system to be designed before starting to code, but it also encourages rapid, and continuous feedback. Scenario Hunting lets design and implementation be accomplished asynchronously and without interrupting each other. In fact separation of design and implementation by time, not only reduces the gap between design and implementation, but it also accelerates the development of cohesive tiny features. Scenario Hunting is the quickest way to drill down, spike, test, and implement the treditional models from board.

<br/>

# Hunting strategy:
The scenario hunters should decide which scenarios to hunt for first. We do not dictate which scenarios should be hunted for first. But some heuristics might help to decide. Imagine a situation in which we get stuck with a decision that a stakeholder needs to involve. The speed of the team is as slow as the stakeholder in this situation. On the other hand not all decisions are that important that a bussy stakeholder needs to be involved. As an example a simple decision about an authentication service which is not the core of the problem domain. The decision can be made by developers locally, and the hunting for such scenarios can be postponed, to avoid wasting the time of the whole team.

So which scenarios to hunt first?
Here are some heuristics:
- When core domain features are unclear due to technical uncertainties: Start hunting from the core domain features (because core features affect the rest of the features).
- When technical affordability is uncertain in features that the other important features depend on them: Start hunting scenarios from the most responsible scenarios.
- When releasing a specific set of features are the most important: Start hunting for scenarios from those features.
- When knowledge discovery and model consistency is more important than quick delivery; Hunt the most ambiguous scenarios first.




<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<hr />






-   User guide (TBD)

    -   Scenario Hunting (TBD)

        -   Introduction  (TBD)

        -   Practical guide  (TBD)
        
            -   Getting started  (TBD)

                -   Installation  (TBD)

                -   Modeling a simple story (TBD)

                -   Hunting a scenario (TBD)

                -   Building a template  (TBD)

                    -   Write the test manually  (TBD)

                    -   Template studio  (TBD)

                    -   Repel drive the template  (TBD)

            -   Hunting unit scenarios  (TBD)

                -   Aggregate  (TBD)

                -   read model  (TBD)

                -   policy (TBD)

                -   service  (TBD)

            -   Hunting API acceptance scenarios  (TBD)

            -   Hunting UI acceptance scenarios  (TBD)

            -   Hunting integration scenarios  (TBD)

            -   Hunting contract driven scenarios  (TBD)

            -   Example mapping the scenarios (TBD)

        -   Conceptual guide (TBD)

            -   Model Exploration Whirlpool (TBD)

            -   Levels of abstraction  (TBD)

            -   The users (TBD)

            -   The problem (TBD)

            -   The solution (TBD)

            -   The contract  (TBD)

            -   The power of abstraction  (TBD)

            -   Abstract Bddd (TBD)

            -   Virtual Facilitation (TBD)

            -   Hunting prioritization  (TBD)

            -   When to hunt a scenario  (TBD)

            -   When not to extract the test code (TBD)

        -   Design guide (TBD)

            -   Roles (TBD)

            -   Programming Language agnosticism  (TBD)

            -   Paradigm agnosticism  (TBD)

            -   Design style  (TBD)

                -   White box vs black box (TBD)

                -   Unit testing  (TBD)

                    -   Event sourced  (TBD)

                    -   Non event sourced (TBD)

                    -   CRUD (TBD)

                -   Acceptance testing (TBD)

                    -   API (TBD)

                    -   UI (TBD)

                -   Integration testing  (TBD)

                -   Contract Driven testing  (TBD)

                -   Separation of abstraction from  (TBD)implementation integration

    -   Template building (TBD)
            
        -   Learn by doing (TBD)

        -   Start by writing the test manually  (TBD)

        -   Building aggregate templates  (TBD)

        -   Building read model templates  (TBD)

        -   Building policy templates  (TBD)

        -   Building services templates  (TBD)

        -   Building api acceptance templates  (TBD)

        -   Building ui acceptance templates (TBD)

        -   Building integration templates  (TBD)

        -   Building contract driven templates  (TBD)

        -   Handlebars (TBD)

            -   Language introduction  (TBD)

            -   Built-in functions (TBD)

        -   Syntax highlighting  (TBD)

        -   Intellisense  (TBD)

        -   Error handling  (TBD)

        -   Repel driven development (TBD)

    -   Event storming  (TBD)

    -   Event modeling (TBD)

    -   Example mapping (TBD)

    -   Bdd (TBD)

    -   Ddd (TBD)

    -   Agile (TBD)

-   Contribution guide (TBD)
