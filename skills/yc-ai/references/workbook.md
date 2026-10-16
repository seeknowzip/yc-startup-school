# Guided workbook

Read only for a requested worksheet, guided practice, or diagnostic. Use the questions as prompts, adapting to the user's goals, stage, and already supplied evidence. Provide the full worksheet when requested; for interactive practice ask a manageable question and wait, using an available interface or ordinary chat. Offering a few answer options can make a question easier to answer. After each answer, respond briefly and connect it to the relevant talk before moving on. Skip irrelevant or answered prompts and respect requests to stop.

Ground feedback in relevant original passages. Separate the user's answers from your interpretation; describe supported strengths, uncertainties, and a useful next step. Score only when requested and explain the rubric and uncertainty. Do not infer character or competence from missing answers.

Save only when the user requests a file. Use their destination; if none is specified for an explicit save request, use a `yc-startup-school-notes/` folder in the current working directory with a descriptive dated filename and preserve existing files. Otherwise finish in conversation. Record partial work as partial.

## Question bank

1. Are you using AI as a copilot, a software factory, or a set of self-improving company loops? Which scope fits your goal, and what evidence would justify changing it? (Garry Tan in the Stanford CS153 talk; Tom Blomfield, "How to Build a Self-Improving Company with AI")
2. Which important company signal is currently not recorded, summarized, or retrievable by agents? (Tom Blomfield, "How to Build a Self-Improving Company with AI": if it is not recorded, it did not happen to your intelligence)
3. Pick one workflow you are considering for automation. What would be its sensor layer, policy/decision layer, deterministic tools, quality gates, and learning mechanism? (Tom Blomfield, "How to Build a Self-Improving Company with AI")
4. What should become a skill, what should become a resolver route, what should become a deterministic tool, and what should become an eval? (Garry Tan: skills/resolvers/memory/evals as org primitives)
5. Where does human taste still need to judge traces, outputs, customer trust, or business outcomes? (Diana Hu: taste becomes evals)
6. Is your next idea concrete enough — specified in enough detail that an engineer could go and build it? With AI making quick prototypes far faster to build (his estimate: easily 10x), is your bottleneck engineering or getting user feedback and deciding what to build? (Andrew Ng)
7. Is your product closer to an Iron Man suit — a partial-autonomy product with a fast human generation-verification loop and an autonomy slider you can move toward more autonomy over time — or a flashy autonomous demo? (Andrej Karpathy: partial autonomy apps, advice for "this stage" of working with fallible LLMs; he wants "a bit of both" augmentation and agents)
8. Does using your product or operating workflow improve future runs — traces captured, failures turned into evals, fixes replayed into the system? (Diana Hu; "How to Build a Self-Improving Company with AI")
9. If a future model could replicate your product from a prompt, what would still make you hard to replace? Which painful customer workflow have you gone deep enough into to own? (Jordan Fisher: what's your moat?; Diana Hu: workflow wedge; contrast Andrew Ng: moats tend to be overhyped, the first focus is a product users want, and more businesses start with a product and evolve into a moat)
10. Which AI theme is most directly relevant to your product — and which is most threatening to your current approach?
