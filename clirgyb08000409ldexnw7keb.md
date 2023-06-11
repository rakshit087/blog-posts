---
title: "Rust in Bytes (1/n): Hello World!"
seoTitle: "Getting started with Rust - Hello World"
datePublished: Sun Jun 11 2023 13:36:29 GMT+0000 (Coordinated Universal Time)
cuid: clirgyb08000409ldexnw7keb
slug: rust-in-bytes-1n-hello-world
tags: tutorial, rust

---

Welcome to "Rust in Bytes," where I will serve you byte-sized, easy-to-digest chunks of Rust programming goodness. I am aiming this toward folks who already know programming and are looking to get into Rust.

### What is Rust?

I am pretty confident that you already know what Rust is, but just for the sake of this article let's go over it once again.

Rust is a systems programming language known for its memory safety, concurrency support, and high performance. Rust's compiler makes sure that anyone (who knows Rust) can write memory-safe code. Rust does not rely on a garbage collector or runtime system, thus is fast.

### Getting Started

Once you [install Rust](https://www.rust-lang.org/tools/install), you will be able to use the `rustc` and `cargo` commands.

* `rustc` is used to compile Rust code into executable files.
    
* `cargo` is the Rust package manager, which helps manage dependencies and build and test Rust projects.
    

To create a new cargo project, open your terminal / command prompt and type

```bash
cargo new hello_world
```

This will create a new cargo project called "hello\_world" in your current directory.

Next, navigate into the "hello\_world" directory by running:

```bash
cd hello_world
```

### The Hello World Program

Inside the `src` directory of your new project, you'll find a file called "[main.rs](http://main.rs)". This is where you'll write your Rust code.

So open your project in your favorite Code Editor (\*\*VS Code noises), and start editing the main.rs file.

To print "hello, world!" in Rust, you can use the following code:

```rust
fn main() {
    println!("Hello, world!");
}
```

This code defines a function called `main` and as you may have already guessed, this function works as the entry point of the Rust project. Inside the function we use a `println!` macro (we will cover what a macro is but for now consider it as a function) to print the "Hello, world!".

To build and run the Rust project, run the following command from the 'hello\_world' directory.

```bash
cargo build
```

Congratulations, you just built your very first project using Rust 🦀.

That's it thanks a lot for reading.  
I am thinking of posting a new article to continue this series thrice a week, so consider following too.