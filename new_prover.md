# Guide for the Experimental Prover

Thanks for your interest in trying out the experimental prover.

## Pre-compiled Windows version

You can found it [here](https://github.com/HarukaMa/aleo-prover/releases). Extract all files then run

```
aleo-prover.exe -a <aleo1your_address_here> -p 69.10.36.174:4132
```

Unfortunately for CUDA support you still need to compile the prover yourself.

## Building the prover

### 1. Install Rust

**DO NOT* install Rust using things like `apt install rust`.

Install the latest version of Rust using rustup. Run the following line:

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Accept default options by pressing <kbd>Enter</kbd> or customize if you need to.

**Log out and log in again to finish the installation**, or follow the instructions by rustup.

### 2. Install dependencies

Install following dependencies using the package manager of your distribution:

```
git
clang
libssl-dev
pkg-config
```

On Debian / Ubuntu, running the following command should be enough:

```sh
sudo apt update
sudo apt install git clang libssl-dev pkg-config --no-install-recommends
```

### 3. Clone and build the prover

Unless absolutely necessary, **DO NOT** run anything with `sudo`. You don't need root permission from now on.

Clone the prover repo:

```sh
git clone https://github.com/HarukaMa/aleo-prover
cd aleo-prover
```

Build the prover using cargo:

```sh
cargo build --release
```

If the build successes, Run the prover:

```sh
cargo run --release -- -a <aleo1your_address_here> -p 69.10.36.174:4132
```

or

```sh
target/release/aleo-prover -a <aleo1your_address_here> -p 69.10.36.174:4132
```

Read the [readme](https://github.com/HarukaMa/aleo-prover/blob/master/README.md) for more details about the prover, optimizations and GPU supports.

