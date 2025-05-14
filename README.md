# Smart Home System — Maude Specification

This project models a smart home system using Maude. It supports devices like sensors and actuators, applies environment effects, and simulates automation rules. It is written using a **functional programming approach**, with support for **model checking**.

## 📁 File Naming Convention

- `*-fn.maude`: Files using a **functional style**. These files define the static structure, behavior, and rules of the smart home system.
- `*-mc.maude`: Files related to **model checking**. These are used to trace and simulate the system's execution over time.
- `model-checker.maude`: Core module providing definitions and utilities for model checking (e.g., configuration tracing, transition logic). NB! This is not included in the repository and is expected to be available in the same folder as the provided code.

## How to Run

To run the system **in the expected order**, follow these steps:

1. **Load the model checker core definitions**:
   ```maude
   load model-checker.maude
   ```

2. **Load the smart home system written in functional style**:
   ```maude
   load smarthome-fn.maude
   ```

3. **Load the model checking setup and test suite**:
   ```maude
   load smarthome-mc.maude
   ```

You can now run test cases, simulate rule application, and trace the behavior of the smart home system using commands like:
```maude
red trace(5, < coldConfig >) .
```

All test cases can be found in `smarthome-fn.maude`

## Notes

- This setup assumes you are using the [Maude system](https://maude.cs.illinois.edu/) with all files located in the same directory.
