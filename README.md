# Brihas (Product Updates)

| Update | Category | What changed | Impact |
|---|---|---|---|
| **Proactive sourcing** (waits for user → acts autonomously) | Quality | Solved limited candidate pools caused by narrow, user-driven searches requiring multiple prompts to expand | Broader search coverage from the first run; no manual prompt iteration needed to surface more candidates |
| **Search engine swap** (Google → Exa neural search) | Quality | Web researcher uses Exa's semantic search instead of keyword search — finds candidates by meaning, not exact words. E.g. searching *"VP of Sales"* also surfaces profiles where the person is described as *"leads all revenue and go-to-market"* — Google would miss this entirely since the words don't match | 20× more accurate per SimpleQA benchmark; surfaces passive & hidden C-level candidates Google misses entirely |
| **Parallel sourcing** (batch size 2 → 10, sequential → simultaneous) | Speed | Sourcer now fires all batches at once instead of waiting for each pair to finish before starting the next | ~25× faster pipeline wall-clock time |
| **Sourcer model** (Sonnet 4.6 → Haiku 4.5) | Speed | Replaced the heavier Sonnet model on the sourcer agent with the faster, Haiku model | ~4× faster per sourcer call; |
| **Model-agnostic architecture** (hard-coded → plug-and-play) | Infrastructure | Orchestration logic fully decoupled from inference layer — each agent's model is a single config value, swappable independently | Zero rewrite cost when new models drop; mix best-in-class models per agent role as the landscape evolves |
