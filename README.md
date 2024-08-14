# 0g-da-retriever-guide
This guide will help you to put da retriever without any problems

# 🐕 DA Retriever Setup Guide

This guide will help you set up your own **DA Retriever** from **0G Labs**. Follow these steps to get everything up and running smoothly.

## 💻 **Hardware Requirements**

To ensure optimal performance, your device should meet the following recommended hardware specifications:

- **RAM**: 8 GB
- **CPU**: 2 cores
- **Bandwidth**: 100 MBps (Download / Upload)

## 🛠️ **Installation**

### 1. **Install Dependencies**

Before you begin, make sure to install the necessary dependencies.

#### For Linux 🐧

Update your package manager and install the required packages:

```bash
sudo apt-get update
sudo apt-get install cmake build-essential protobuf-compiler
```

#### For macOS 🍏

Use Homebrew to install CMake:

```bash
brew install cmake
```

### 2. **Install Rust 🦀**

Rust is required to build the DA Retriever. Install Rust using the following command:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### 3. **Download the Source Code 📥**

Clone the DA Retriever repository to your local machine:

```bash
git clone https://github.com/0glabs/0g-da-retriever.git
```

## ⚙️ **Configuration**

Before running the retriever, you need to configure it properly. Here are the key configuration fields:

| Field                 | Description                                                    |
|-----------------------|----------------------------------------------------------------|
| `log_level`           | Set the logging level for the application (e.g., `info`, `debug`). |
| `grpc_listen_address` | The server address where the retriever will listen for gRPC connections. |
| `eth_rpc_endpoint`    | The JSON RPC endpoint for connecting to the blockchain network.  |

Update the `run/config.toml` file with your desired settings.

## 🚀 **Run DA Retriever**

### 1. **Build the Project in Release Mode**

First, build the project for optimized performance:

```bash
cargo build --release
```

### 2. **Start the Retriever 🏃‍♂️**

With your configuration file (`run/config.toml`) properly set up, run the retriever using:

```bash
./target/release/retriever --config ./run/config.toml
```

## 💡 **Tips and Troubleshooting**

- **Slow Performance?** Make sure your device meets the hardware requirements and that you are connected to a stable, high-speed internet connection.
- **Log Level Issues?** Adjust the `log_level` in your config file to `debug` to get more detailed logs if you run into issues.

---

Thank you for choosing **DA Retriever** from **0G Labs**! If you have any questions or run into issues, feel free to reach out to our support team. 😊
