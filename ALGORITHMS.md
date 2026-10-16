# Algorithms and trade-offs

## Reflex decision-making

A reflex agent evaluates the immediate successor state rather than
searching multiple turns ahead. It is computationally inexpensive but
can miss longer-term consequences.

## Minimax

Minimax treats Pacman as the maximizing agent and ghosts as minimizing
agents. This gives a robust decision under the assumption that ghosts
choose actions that minimize Pacman's evaluation.

## Alpha-beta pruning

Alpha-beta maintains bounds on outcomes during minimax traversal. Branches
that cannot change the selected decision are skipped, reducing search
work in favorable cases while preserving the minimax choice.

## Expectimax

Expectimax replaces minimizing ghost nodes with expected-value nodes.
This project models legal ghost actions as uniformly random. That model
may be unrealistic for adaptive adversaries but demonstrates the impact
of uncertainty assumptions.

## State evaluation

A heuristic evaluator can combine multiple signals such as score,
remaining food, proximity to pellets and capsules, ghost distance, and
frightened-ghost duration. The trade-off is that weights are hand-chosen
and may not generalize across all maps or ghost strategies.

## Comparison

| Dimension | Minimax | Alpha-beta | Expectimax |
|---|---|---|---|
| Opponent model | Worst-case | Worst-case | Probabilistic |
| Decision criterion | Maximize minimum utility | Same as minimax | Maximize expected utility |
| Search savings | None by default | Pruning | None by default |
| Main limitation | Can be overly conservative | Depends on move order | Depends on accurate opponent model |
