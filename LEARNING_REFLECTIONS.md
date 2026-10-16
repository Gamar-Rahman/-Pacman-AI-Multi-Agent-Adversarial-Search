# Learning reflections

This project illustrates three distinctions that matter in applied AI:

1. **A rational choice depends on the opponent model.** Planning for the
   worst case and planning for the average case can produce different actions.
2. **Computation is a resource constraint.** Pruning and evaluation
   functions make deeper planning more practical.
3. **An evaluation function is a design decision.** Combining rewards,
   threats, and remaining objectives influences agent behavior even when
   the underlying search algorithm is unchanged.

## Application to security operations

Cloud and SOC environments involve competing objectives and uncertain
observations. Adversarial search provides a way to think about attacker
responses; expectimax provides a contrasting framework for uncertainty;
and evaluation design emphasizes prioritizing risks and objectives.

These connections are conceptual and should not be mistaken for a deployed
security product or a validated threat-detection model.
