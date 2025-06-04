# ctftimer.curses

A terminal-based interactive calculator to compute a custom **team rating** using a weighted formula. Built with Python and `curses`.

## Features

- Navigate and edit fields interactively
- Live calculation of rating based on inputs
- Clean curses-based UI

## Formula

$$
\text{points\_coef} = \frac{\text{team\_points}}{\text{best\_points}} \\
\text{place\_coef} = \frac{1}{\text{team\_place}} \\
\text{rating} = (\text{points\_coef} + \text{place\_coef}) \times \text{weight} \div \left( \frac{1}{1 + \frac{\text{team\_place}}{\text{total\_teams}}} \right)
$$


## Inputs

- **Weight** (float)
- **Total Teams** (int)
- **Best Points** (float)
- **Team Place** (int)
- **Team Points** (float)

## Controls

- **↑ / ↓**: Navigate fields
- **Tab / Shift+Tab**: Cycle through fields
- **Type**: Directly edit fields
- **Backspace / Delete**: Modify input
- **ESC**: Exit

## Requirements

- Python 3.x
- Unix-based terminal (for `curses` support)

## Run

```bash
./team_score
```

## Notes

* First keystroke in a field clears its default value
* Invalid entries are ignored in real time

