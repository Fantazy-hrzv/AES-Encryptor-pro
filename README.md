# AES Encryptor Pro

A modern, password‑based AES‑256 encryptor for **messages** and **files** with a clean dark UI, drag‑and‑drop, key saving, and one‑click copy. Built with Python (Tkinter + PyCryptodome) and packaged as a Windows .exe.

---

## ✨ Features

* AES‑256 (CBC) with PBKDF2 key derivation (salted, 100k iterations)
* Encrypt / Decrypt messages (Base64 text)
* Encrypt / Decrypt files (any file type)
* Password input with salted key derivation (no raw key files needed)
* Save / Load key info (`.key` files contain Base64 salt + IV)
* Drag & drop box for quick file encrypt/decrypt
* Read‑only output + Copy Output button
* Help popup (in‑app) and status bar messages
* Dark, spacious UI with placeholders and top‑right utility buttons

> **Note:** Losing the password or the saved `.key` associated with an encrypted payload means the data cannot be recovered.

---

## 🚀 Quick Start (Windows EXE)

If you have the packaged `.exe` (or installed via the Setup Installer):

1. Run `AES Encryptor Pro.exe`.
2. Use the steps below to encrypt/decrypt messages or files.

No Python installation is required for the `.exe` build.

---

## 🐍 Quick Start (Run from Source)

**Requirements:**

* Python 3.9+ (3.11 supported)
* `pycryptodome` and (optional) `tkinterdnd2`

**Install dependencies:**

```bash
python -m pip install -r requirements.txt
```

**Run the app:**

```bash
python aes_encryptor_final_ui.py
```

---

## 🧭 Using the App

### Encrypt a Message

1. Enter a password.
2. Type the message.
3. Click **Encrypt Message**.
4. Copy or save the output.
5. Optional: Save the key file.

### Decrypt a Message

1. Enter the same password.
2. Paste the ciphertext.
3. Optional: Load the `.key` file.
4. Click **Decrypt Message**.

### Encrypt a File

1. Enter a password.
2. Click **Encrypt File**.
3. Select your file.
4. Optional: Save the key file.

### Decrypt a File

1. Enter a password.
2. Optional: Load the `.key` file.
3. Click **Decrypt File**.
4. Select your file.

### Drag & Drop

Drop a file into the box to encrypt or decrypt.

---

## 🔐 Security Notes

* AES‑256 CBC + PBKDF2, 100k iterations.
* `.key` stores only salt & IV, no password.
* No password storage.
* If password and key are lost, decryption is impossible.
* File operations overwrite originals — work on copies if needed.

---

## 📦 Packaging (EXE)

Build with:

```bash
python -m pyinstaller --noconsole --onefile --icon=encryptor.ico aes_encryptor_final_ui.py
```

---

## 📄 License

See `LICENSE.txt` for the full license terms.

---

## 🙌 Credits

* PyCryptodome for cryptography primitives
* Tkinter for UI
* TkinterDnD2 for drag‑and‑drop support

---

## 📄 LICENSE.txt

```
Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)

You are free to:
- Share — copy and redistribute the material in any medium or format.

Under the following terms:
- Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- NonCommercial — You may not use the material for commercial purposes.
- NoDerivatives — If you remix, transform, or build upon the material, you may not distribute the modified material.

No warranties are given. The license may not give you all of the permissions necessary for your intended use.

Full legal code: https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode
```
