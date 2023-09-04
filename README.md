# Intro to Rust - Build a State Machine

These exercises are to accompany the Intro to Rust course by Web3 Foundation, which in turn is to augment the Rust book itself.  The primary goal of these is to provide a self-gradable way to learn Rust in the context of blockchain, and eventually Substrate.

## Exercise Structure & Goal

Goal: **create a state machine that resembles a blockchain-like protocol.**

A state machine is something that is the essence of any web3 or blockchain related protocol. Particuarly, fintite-state machines most accurately describe these systems:

> **Finite-state machine**
> 
>A finite-state machine (FSM) or finite-state automaton (FSA, plural: automata), finite automaton, or simply a state machine, is a mathematical model of computation. It is an abstract machine that can be in exactly one of a finite number of states at any given time. The FSM can change from one state to another in response to some inputs; the change from one state to another is called a transition.
>
> [Source Wikipedia - Finite State Machine](https://en.wikipedia.org/wiki/Finite-state_machine)

As a programmer, all one is doing is providing input from to change something from one state to another.  Whether that's the program written, or the language itself, state machines are an integral part of many modern day systems, not just blockchains!

Some common examples of finite-state machines in everyday life are:

- On-and-off switches (two states: on, or off, depending on the current state and input)
- Vending machines (the output is dictated by the input, aka, how many coins will dictate which snack is dispensed).
- Computers, calculators, etc.

Particularly, we will focus on a **finite** state machine.  A finite state machine is simply a state machine that has a finite, or fixed, number of states that it can be in.  For example, a light switch can only be in one of two states: on or off.


### How does this relate to our project?    

Blockchain, at its core, represents a finite state machine in many ways. In the most primitive manner, a blockchain simple goes from S<sup>o</sup> --> S<sup>n</sup>, where S<sup>n</sup> represents the new state, which builds on the old state, S<sup>o</sup>.

In the context of a blockchain, we want to be able to build from block `0` forwards, with each block building on the data from the previous block.  We will also touch on some basics with generic code design and the exact reasons for *why* we have structured our state machine.

There are a number of parameters that go into a state machine, such as a blockchain.  These terms will be introduced as needed.


### How do I follow along?

1. Ensure Rust is installed on your system: [Install Rust](https://education.web3.foundation/docs/Rust/setup/installation)

2. Clone this repository:
   
    ```bash
    git clone git@github.com:w3f/intro-to-rust-exercises.git
    ```

3. Make the unit tests for each exercise pass by implementing the `todo!()`s' spread throughout each exercise. (see:[ Checking Answers & Testing](#checking-answers--testing))

Refer to either the Rust Book, or our course on the Web3 Foundation's Education to get an idea on the concrete concepts represented through out the excercises


## Checking Answers & Testing

This project operates on a series of unit tests that are included with each exercise.  Your job is to ensure all unit tests pass for all of the exercises.  It is assumed that Rust is installed on your system, and `cargo`, Rust's package manager and build tool, is in your `PATH`.

For running for a single exercise (`ex01_functions` as an example):

```sh
cargo test ex01_functions
```

For running all exercises: 

```sh
cargo test
```

## Contributing

Spot a way to make things clearer, better, or improve the structure? Feel free to submit a PR, or an issue beforehand to discuss it!


## Resources

Below are supplementary resources to aid in your learning journey.  This aims to be a beginner tutorial, however the following are also fantastic reads:

- [Pretty State Machine Patterns in Rust by Hoverbear](https://hoverbear.org/blog/rust-state-machine-pattern/)
- [Blockchain from Scratch (Rust) by Josh Orndorff](https://github.com/JoshOrndorff/blockchain-from-scratch)

