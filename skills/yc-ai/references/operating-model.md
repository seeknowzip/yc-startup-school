# Operating-model design

Use when the user requests AI workflow or company design. Begin with the actual outcome, existing process, evidence, constraints, and permitted actions. Compare a human process, an assistive tool, partial automation, and a more autonomous loop where relevant; retaining the current process can be a reasonable conclusion.

The two company-operation talks in [the source map](source-map.md) are starting points, not a mandatory architecture. Read relevant original passages and use other talks only when they inform the decision.

For the chosen workflow, make clear what information is available, what needs judgment, what can be deterministic, how quality is evaluated, who handles exceptions, and what feedback could improve it. Separate observed capabilities from proposed changes. A table can help compare functions but is not required for a definition or a small recommendation.

A proposed learning loop needs a way to detect regressions and decide whether a change is better. Logs or increased token use alone do not prove improvement. Relate evaluation to the user's outcome, cost, latency, and failure consequences. Do not mandate skills, resolvers, memory, agents, or a company-wide migration where simpler means suffice.

Finish the requested design with its assumptions and a proportionate next validation step. A design request does not authorize deploying automation, collecting private company data, contacting customers, or changing live systems.
