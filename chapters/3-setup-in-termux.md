

# 📘 Chapter 3: Shell Scripting in Termux



---

## ✍️ What is Shell Scripting?

Shell scripting allows you to write a sequence of commands in a `.sh` file that the terminal can execute automatically.
It helps automate tasks like backups, installations, and setups.

---

## 🧱 Shell Script Structure

A basic shell script looks like this:

```bash
#!/bin/bash

echo "Hello, World!"
```

* `#!/bin/bash`: Tells Termux to use the bash shell.
* `echo`: Prints text to the screen.

---

## 🗂️ Creating and Running a Shell Script

### 1. **Create the File**

```bash
touch script.sh
```

### 2. **Edit the File**

```bash
nano script.sh
```

➡️ Paste this inside:

```bash
#!/bin/bash
echo "Welcome to CodeSaif's Shell Script!"
```

To save in `nano`: Press `CTRL + X`, then `Y`, then `Enter`

### 3. **Make it Executable**

```bash
chmod +x script.sh
```

### 4. **Run the Script**

```bash
./script.sh
```

---

## ✅ Examples

### 🧪 Example 1: Show Date and Time

```bash
#!/bin/bash
echo "Current Date and Time:"
date
```

### 🧪 Example 2: Make a Directory Automatically

```bash
#!/bin/bash
mkdir termux-practice
cd termux-practice
echo "Created and moved into termux-practice"
```

### 🧪 Example 3: Backup a File

```bash
#!/bin/bash
cp important.txt backup_important.txt
echo "Backup created"
```

---

## 📌 Tips

* Always use `.sh` extension for shell scripts.
* Use `chmod +x` every time you make a new script.
* You can run scripts from anywhere using: `bash yourscript.sh`

---

Next: [Chapter 4 → Basic Git Commands](#)
