Here’s a clean, structured **step-by-step document** you can use as training or project notes for setting up EC2, Git, and GitHub.

---

# 🚀 Launching EC2, Configuring Git, and Connecting GitHub

## 1️⃣ Launching an EC2 Instance (Amazon Linux)

1. **Login** to [AWS Console](https://console.aws.amazon.com/).
2. Search for **EC2** service.
3. Launch a new instance with:

   * **AMI**: Amazon Linux 2023
   * **Instance type**: `t3.micro` (Free Tier eligible)
   * **Key pair**: Download `key.pem`
   * **Security Group**: Allow **SSH (22)** from `0.0.0.0/0`
4. Once launched, copy the **Public DNS** of the instance.

### SSH into EC2

```bash
ssh -i "key.pem" ec2-user@ec2-3-80-195-140.compute-1.amazonaws.com
```

---

## 2️⃣ Install and Configure Git

Update packages and install Git:

```bash
sudo yum update -y
sudo yum install git -y
git --version
```

Configure Git:

```bash
git config --global user.name "Atul Kamble"
git config --global user.email "atul_kamble@hotmail.com"
git config --list
```

---

## 3️⃣ Setup GitHub Account

1. Sign up or log in to [GitHub](https://github.com/).
2. Create a new repository (example: `myrepo`).
3. Add:

   * `README.md`
   * License (MIT recommended)

### Edit `README.md`

Example:

```markdown
# My First Repo

This is my practice repository.

```

echo "hello"

```

1. Step One
2. Step Two
3. Step Three
```

---

## 4️⃣ Clone Repository to EC2

Clone the repo:

```bash
git clone https://github.com/atulkamble/mynewrepo.git
cd mynewrepo
```

---

## 5️⃣ Test with Python File

Create a simple Python file:

```python
# helloworld.py
print("Hello World from EC2 + GitHub!")
```

Run it:

```bash
python3 helloworld.py
```

---

✅ **You have successfully launched an EC2, installed Git, configured GitHub, cloned your repo, and tested Python code.**

---

Would you like me to **package this into a `README.md` (with emojis and code blocks)** so you can directly push it to your GitHub repo as project documentation?
