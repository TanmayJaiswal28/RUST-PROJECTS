# RUST-PROJECTS – Rust learning playground

A minimal collection of Rust examples. The repository currently contains a single command‑line implementation of the classic **Bulls & Cows** (number‑guessing) game.

## Overview

`Bulls&CowsInRust/main.rs` is a self‑contained program that:

* Generates a secret number between 1 and 10 using the `rand` crate.  
* Prompts the user for a guess, validates numeric input and the 1‑10 range.  
* Gives feedback (`too small!`, `too big!`, or success).  
* Tracks attempts, shows a tip after the 5th try, and ends after 10 attempts or a correct guess.

The code uses only the Rust standard library (`std::io`, `std::cmp::Ordering`) plus `rand::Rng`.

## Repository structure

```
RUST-PROJECTS/
├─ .gitattributes
└─ Bulls&CowsInRust/
   └─ main.rs   ← entry point for the Bulls & Cows game
```

## Running the game

1. **Install Rust** (if not already installed)

   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. **Clone the repository**

   ```bash
   git clone https://github.com/TanmayJaiswal28/RUST-PROJECTS.git
   cd RUST-PROJECTS/Bulls&CowsInRust
   ```

3. **Compile and run**

   The source depends on the external `rand` crate, so a Cargo project is required. You can create one quickly:

   ```bash
   cargo init --bin .
   echo 'rand = "0.8"' >> Cargo.toml   # add the dependency
   cargo run
   ```

   If you prefer to compile with `rustc`, you must first obtain the `rand` crate source and link it manually, which is more involved.

   The program will display:

   ```
   Welcome to Bull and Cows
   Please input a number:
   ```

   Follow the prompts to play.

## Current status & limitations

* Only the Bulls & Cows example is present; no test suite, CI configuration, or additional projects are included.  
* A `Cargo.toml` file is not part of the repository, so you need to create one to resolve the `rand` dependency.  
* The program runs on any platform supported by Rust (Linux, macOS, Windows) with a terminal that accepts standard input.

## Contributing

Contributions that add more Rust examples are welcome.

1. Fork the repository.  
2. Create a new directory for your example (e.g., `LinkedListExample/`).  
3. Add source files and, if needed, a `Cargo.toml` with required dependencies.  
4. Ensure the code builds with `cargo build` / `cargo run`.  
5. Submit a pull request describing the new example.

---

Repository: https://github.com/TanmayJaiswal28/RUST-PROJECTS (last push: 2025‑04‑20)
