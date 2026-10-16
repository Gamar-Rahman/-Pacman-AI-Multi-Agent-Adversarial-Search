# Testing and limitations

## Test coverage

The implementation was evaluated with the course-provided Pacman autograder
for five parts: reflex agent, minimax, alpha-beta, expectimax, and an
improved evaluation function. The local score was **25/25**.

| Test section | Local points |
|---|---:|
| Q1 — Reflex agent | 4/4 |
| Q2 — Minimax | 5/5 |
| Q3 — Alpha-beta pruning | 5/5 |
| Q4 — Expectimax | 5/5 |
| Q5 — Evaluation function | 6/6 |
| **Total** | **25/25** |

The supplied Q1 reflex-agent test won **10/10 games** with an average
score of **1,315.1**. The Q5 evaluation-function test also won **10/10 games**
with an average score of **1,062.2**. These are outcomes on the
course-provided local test configurations, not broad claims about performance
across all game settings.

**This does not imply** that every possible state, layout, or ghost policy
has been tested, nor does it represent a production-grade system or
an official Gradescope grade.

## Limitations

- The game environment is a simplified, fully specified turn-based model.
- Minimax assumes worst-case ghost responses.
- Expectimax assumes a probability distribution over ghost actions.
- Hand-designed evaluation features can be sensitive to weights and maps.
- Search grows rapidly with branching factor and depth.
- Security analogies are educational, not empirical SOC performance claims.

## Reproducibility and academic integrity

The full code and original autograder are not publicly shared because the
starter-project notice explicitly prohibits publishing solutions.
Conceptual documentation is provided for technical discussion and portfolio
review without exposing graded implementations.
