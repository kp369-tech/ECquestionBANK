# ECquestionBANK


## Cloning This Repository Using SSH

### 1. Generate an SSH Key (if you don't have one)

Open your terminal and run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

*If your system doesn't support `ed25519`, use:*

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- Press Enter to accept the default file location.
- Set a passphrase if you want, or press Enter for no passphrase.

**Reference:** [GitHub Docs: Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

---

### 2. Add Your SSH Key to the SSH Agent

Start the SSH agent and add your key:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
*(Use the correct filename if you named your key differently.)*

---

### 3. Add Your Public Key to GitHub

- Copy your public key to the clipboard:

  ```bash
  cat ~/.ssh/id_ed25519.pub
  ```

- Go to [GitHub SSH Keys Settings](https://github.com/settings/keys).
- Click **New SSH key**, paste your key, and save.

---

### 4. Clone the Repository Using SSH

```bash
git clone git@github.com:kp369-tech/ECquestionBANK.git
```

---

### 5. Test Your SSH Connection (Optional)

```bash
ssh -T git@github.com
```

You should see a welcome message if everything is set up correctly.

---

### 6. Push File into repo
```bash
git push origin main
```



**More Info:**  
- [GitHub Docs: Connecting to GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
