# 🚀 ServerHub Agent Installation Guide

Welcome to the **ServerHub Agent** installation guide! Follow these simple steps to set up and start using the ServerHub Agent on your system.

---

## 📋 Prerequisites

Before starting, ensure you have the following:

- ✅ A Debian-based Linux distribution (e.g., Ubuntu).
- ✅ `sudo` privileges to install packages.
- ✅ Internet access to download the repository and GPG key.

---

## ⚙️ Installation Steps

### 1️⃣ Step 1: Download and Add the GPG Key

The GPG key ensures the authenticity of the ServerHub repository. Run the command below:

```bash
curl -fsSL https://raw.githubusercontent.com/7Stockapp/serverhub/main/serverhub.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/serverhub-archive-keyring.gpg > /dev/null
```

---

### 2️⃣ Step 2: Verify the GPG Key Fingerprint

Check if the GPG key has been added correctly:

```bash
gpg --no-default-keyring --keyring /usr/share/keyrings/serverhub-archive-keyring.gpg --list-keys
```

---

### 3️⃣ Step 3: Add the Repository

Add the ServerHub repository to your system’s package list:

```bash
echo "deb [signed-by=/usr/share/keyrings/serverhub-archive-keyring.gpg arch=amd64] https://raw.githubusercontent.com/7Stockapp/serverhub/main/ stable main" | sudo tee /etc/apt/sources.list.d/serverhub.list
```

---

### 4️⃣ Step 4: Update and Install

Update your package lists and install the **ServerHub Agent**:

```bash
sudo apt update && sudo apt install serverhub-agent
```

---

## 🎉 Success!

The **ServerHub Agent** is now installed on your system! You’re ready to start using it. 🛠️

---

## ❓ Troubleshooting

If you encounter any issues during the installation:

- 🔍 Ensure your internet connection is stable.
- 🔑 Verify you have the required `sudo` permissions.
- 🛠️ Open an issue in the [GitHub Issues](https://github.com/7Stockapp/serverhub/issues) section for further assistance.

---

## 📄 License

This project is licensed under the https://serverhub.dev/terms-of-use/

---

## 💬 Questions or Feedback?

Feel free to open a discussion or issue in the repository. Your feedback is welcome!

---

> _Created with ❤️ by 7Stockapp OÜ_
