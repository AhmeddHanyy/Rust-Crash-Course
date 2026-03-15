# Rust Crash Course

This repository contains a **Rust crash course taught through interactive Jupyter notebook**.

---

# Running the Notebooks

The notebooks run Rust code using the **evcxr Rust kernel for Jupyter**.

Follow the steps below to set up the environment.

---

# Setup Guide (Ubuntu)

## 1. Install system dependencies

```bash
sudo apt update
sudo apt install -y python3-venv python3-full curl build-essential
```

---

## 2. Install Rust

Install Rust using `rustup`.

```bash
curl https://sh.rustup.rs -sSf | sh
```

Load the Rust environment:

```bash
source $HOME/.cargo/env
```

Verify installation:

```bash
rustc --version
cargo --version
```

---

## 3. Create a Python virtual environment

Ubuntu prevents installing Python packages globally with `pip`, so we use a virtual environment.

```bash
python3 -m venv jupyter-rust
```

Activate it:

```bash
source jupyter-rust/bin/activate
```

---

## 4. Install Jupyter

Inside the virtual environment:

```bash
pip install --upgrade pip
pip install notebook
```

---

## 5. Install the Rust Jupyter kernel

Install the Rust kernel:

```bash
cargo install evcxr_jupyter
```

Register it with Jupyter:

```bash
evcxr_jupyter --install
```

You can verify the kernel is available with:

```bash
jupyter kernelspec list
```

You should see a kernel named `rust`.

---

# Using VS Code (Recommended)

The easiest way to run the notebooks is inside VS Code.

## 1. Install VS Code extensions

Open VS Code and install the following extensions:

* **Jupyter** (Microsoft)
* **Python** (Microsoft)
* **rust-analyzer** (Rust language support)

These extensions enable notebook support and Rust tooling.

---

## 2. Open the repository

Clone the repository:

```bash
git clone https://github.com/AhmeddHanyy/Rust-Crash-Course.git
cd Rust-Crash-Course
```

Open it in VS Code:

```bash
code .
```
