# Engineering philosophy

Reasoned decisions. Practical systems.

That line is the test I use. A decision is reasoned when the problem is framed, the evidence is visible, and a person can explain why this option was chosen. A system is practical when the people who keep it can run it, change it, and trust what it produces. A clever design that nobody can operate is unfinished, and so is a report that nobody can defend.

## Start from the decision

I start from the decision a person has to make, not from a platform or a model. What choice is being supported. What evidence would change it. Which data is fit for that choice. Who is accountable for the answer. If those are still vague, another tool will not clarify them.

The scope of a slice stays small enough to ship and learn from. I use short delivery cycles, and Scrum where it improves the outcome rather than where it only fills a calendar. Each slice should leave the system in a state its owners can explain.

## Build for the people who keep it

Handover is part of the design, not a folder written in the last week. Ownership, access, and the path to production are settled early. Documentation stays lean: the boundaries, the names, and the reasons for the choices that were not obvious.

Pipelines, semantic models, and reports earn their place when a team can run them, see when they fail, and change them without having to guess how they work. Names should describe the business. They should not record which project, environment, or person created the object.

## Governance belongs in the build

Governance is visible from the outset. Access, classification, lineage, and data quality are part of the same design as the tables and the measures. A control that cannot be pointed at in the system is only a hope.

This matters most where the data sits under safety obligations or external scrutiny. Quality, stewardship, and a trace from a figure back to its source are part of what it means to be done.

Security controls are not interchangeable. A workspace role, a row-level filter, and a sensitivity label do different jobs. Applying one does not complete the others. The people who build a system will often be able to see more than the people who read a report. That gap should be a decision, recorded and tested, including with an account that has only the access a real reader will have.

## AI stays inside a human decision

I use AI, including large language models, as a tool inside a system that already has an owner. The model does not repair weak data, and it does not take the accountability that belongs to a person. Before I scale a use case I want a short list answered. Is the underlying data suitable. How is sensitive information protected. How are outputs evaluated. Who remains accountable for the decision. What happens when the output is wrong.

Where a model assists, a person stays in the loop. The model can draft, retrieve, classify, or suggest. It does not become the owner of the decision. An agentic workflow needs a defined scope, an evaluation, and a record of what it did. Without those, it is an experiment, not a system to hand over. I do not want to automate a judgement that cannot be explained afterwards.

## Prefer the simplest design that will hold

Practical does not mean temporary. It means the design has to earn its complexity. A medallion layer, a semantic model, or a deployment pipeline should remove a real failure mode. If a simpler shape will do, use that.

Trade-offs should be written down while the reason is still known. Where a transformation lives, whether the model imports a copy or reads the lake, what is promoted automatically, and what still needs a person: these choices age. A later owner should be able to disagree with them without first reconstructing them.

Reference notes for a few of these patterns are indexed in [reference architectures](reference-architectures/README.md). They are guidance for a class of system, not a record of a particular engagement.
