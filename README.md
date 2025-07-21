#  Java Installation Guide

## Version History

| Author      | Created on | Version   | Last updated by | Internal Reviewer |
|-------------|------------|-----------|------------------|--------------------|
| Anuj Jain   | 17-07-25   | version 1 | N/A              | Prashnat           |

---

##  Table of Contents

1. [What is Java?](#what-is-java)
2. [Check if Java is Installed](#check-if-java-is-installed)
3. [Install Java on Ubuntu](#install-java-on-ubuntu)
4. [Set JAVA\_HOME Environment Variable](#set-java_home-environment-variable)
5. [Verify Java Installation](#verify-java-installation)
6. [Uninstall Java (if needed)](#uninstall-java-if-needed)
7. [References](#references)

---

##  What is Java?

Java is a high-level, object-oriented programming language. It’s platform-independent and widely used in web, desktop, mobile, and enterprise applications.

---

##  Check if Java is Installed

Open a terminal and type:

```bash
java -version
```

If Java is installed, you'll see output like:

```
java version "11.0.22" 2024-04-16 LTS
Java(TM) SE Runtime Environment ...
```

If you get:

```
Command 'java' not found
```

Then Java is not installed.

---

## 💻 Install Java on Ubuntu

### Step 1: Update System

```bash
sudo apt update
```

### Step 2: Install Default Java Runtime Environment (JRE)

```bash
sudo apt install default-jre -y
```

### Step 3: Install Default Java Development Kit (JDK)

```bash
sudo apt install default-jdk -y
```

📝 **Note:** JRE is required to run Java programs. JDK is required to develop Java applications.

---

## 🛠 Set JAVA\_HOME Environment Variable (Optional but Recommended)

### Step 1: Find Java Path

```bash
sudo update-alternatives --config java
```

Output will be something like:

```
/usr/lib/jvm/java-11-openjdk-amd64/bin/java
```

So, JAVA\_HOME is:

```
/usr/lib/jvm/java-11-openjdk-amd64
```

### Step 2: Open `.bashrc` or `.zshrc`

```bash
nano ~/.bashrc
```

### Step 3: Add the following at the bottom:

```bash
export JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"
export PATH="$JAVA_HOME/bin:$PATH"
```

### Step 4: Apply the Changes

```bash
source ~/.bashrc
```

---

##  Verify Java Installation

```bash
java -version
```

And:

```bash
echo $JAVA_HOME
```

If both return correct values, Java is successfully installed.

---

##  Uninstall Java (Optional)

To remove Java completely:

```bash
sudo apt purge openjdk-\* -y
sudo apt autoremove -y
```

---

## Contact Information

| Name      | Email Address                                               |
| --------- | ----------------------------------------------------------- |
| Anuj Jain | [anuj.jain@mygurukulam.co](mailto:anuj.jain@mygurukulam.co) |

---

##  References

* **Official Java Documentation:** [https://docs.oracle.com/en/java](https://docs.oracle.com/en/java)
* **Ubuntu Java Installation:** [https://ubuntu.com/tutorials/install-jdk](https://ubuntu.com/tutorials/install-jdk)
* **JAVA\_HOME Explained:** [https://linuxize.com/post/how-to-set-java-home-in-linux/](https://linuxize.com/post/how-to-set-java-home-in-linux/)

---

