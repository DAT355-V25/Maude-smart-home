# Smart Home System — Maude Specification

This project models a smart home system using the Maude specification language. It defines sensors and actuators as object-oriented components and uses rewrite rules to simulate automation behavior and environmental feedback. The system is evaluated using Maude's built-in Linear Temporal Logic (LTL) model checker to verify correctness.

## File Overview

- `smarthome.maude`: The main specification, including classes, rules, and device logic.
- `smarthome-mc.maude`: Model checking module with LTL formulas and test scenarios.
- `full-maude3.maude`: Full Maude system module.
- `model-checker.maude`: Core LTL model checking logic and configuration.
- `run.maude`: Script for automatically loading all necessary modules in sequence.

## How to Run

1. Open the [Maude system](https://maude.cs.illinois.edu/) and edit the path in `run.maude` to where your folder is located:

From:

```maude
cd "/Users/sanderodegaard/dat355/Maude-3/Maude-smart-home/smarthomesys" .
```

To:

```maude
cd "Your/Path/To/The/Folder" .
```

2. Load the run.maude file after saving by either commandline or in your preferred IDE.

   ```maude
   load run.maude
   ```

   If you did everything correct, the program should be running now.

## 🧪 Example Usage

- Simulate the system:

  ```maude
  rew [8] completeRoom .
  ```

- Run model checking on a safety property:
  ```maude
  red modelCheck(simpleColdRoom, heaterAndFanNotOnSimultaneously) .
  ```

## Notes

- Make sure all `.maude` files are in the same directory before running `run.maude`.
- Examples for what you can verify in the program are located as comments in the bottom of `smarthome-mc.maude`.
