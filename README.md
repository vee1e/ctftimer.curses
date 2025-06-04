# ctftimer.curses

A terminal-based interactive calculator to compute a custom CTFtime **team rating** using a weighted formula. Built with Python and `curses`.

## Features

- Navigate and edit fields interactively
- Live calculation of rating based on inputs
- Clean curses-based UI

## Formula

$$
\text{points-coef} = \frac{\text{team-points}}{\text{best-points}}
$$

$$
\text{place-coef} = \frac{1}{\text{team-place}}
$$

$$
\text{rating} = (\text{points-coef} + \text{place-coef}) \times \text{weight} \div \left( \frac{1}{1 + \frac{\text{team-place}}{\text{total-teams}}} \right)
$$


## Inputs

| Input         | Type  |
|---------------|-------|
| Weight        | float |
| Total Teams   | int   |
| Best Points   | float |
| Team Place    | int   |
| Team Points   | float |

## Controls

| Key/Action           | Function               |
|----------------------|------------------------|
| ↑ / ↓                | Navigate fields        |
| Tab / Shift+Tab      | Cycle through fields   |
| Type                 | Directly edit fields   |
| Backspace / Delete   | Modify input           |
| ESC                  | Exit                   |

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

