🔑 Project 2: The Power of SSH Keys
By Christopher Maximo Castro | CodePath CYB101

🌟 The Big Picture
In this project, I moved beyond passwords. I learned how to generate SSH Key Pairs to handle three of the most critical tasks in security: Authentication (proving who I am), Encryption (keeping data secret), and Integrity (proving a file hasn't been messed with).

My Journey: 🔑 (Generating keys) → 🔒 (Locking data) → 🔗 (Linking my identity to my code)

🏗️ Applying the CIA Triad (SSH Edition)
This week, the CIA Triad wasn't just a theory; I actually built tools to support each pillar:

1. Confidentiality (Asymmetric Encryption): I used openssl and a Public Key to turn a secret message into unreadable gibberish. Only the person with the Private Key could turn it back into plain text.

2. Integrity (Digital Signatures): I learned that a signature isn't just a name at the bottom of an email. In Git, a signature is a mathematical proof. If a single comma in my code is changed, the signature breaks.

3. Availability (Seamless Access): By setting up SSH authentication, I created a way to access my servers securely without relying on passwords that can be forgotten or brute-forced.

--

🕵️ Technical Deep-Dive
1. Asymmetric Encryption: The Minecraft Password Scenario
Imagine needing to send a friend a password. If you send it in plain text, a hacker on your Wi-Fi can see it.

. The Fix: I generated an RSA key pair. I used the Public Key to encrypt secret.txt.
. The Result: Even if an attacker stole the file secret.txt.encrypted, they couldn't read it. Only my Private Key could unlock it to reveal my secret code.
  📸 [SS #1, #2, #3 go here]: I’ve documented the exact openssl commands I used to encrypt and decrypt the message, showing the original text, the encrypted gibberish, and the final recovery.

2. Proving Authorship: Git Commit Signing
In the world of software, you need to know that the code you're downloading actually came from the developer and hasn't been tampered with.

. The Task: I configured Git to use my SSH key as a digital "seal."
. The Moment of Truth: I ran git show --show-signature. Seeing that "Good 'git' signature" message felt like a major win—it's the gold standard for secure coding.
  📸 [SS #4, #5 go here]: These screenshots show the Git commit process and the final verification of my digital signature.

--

🛠️ The Toolkit

. The OS: Ubuntu Linux (Azure Labs)

. The Tools: * ssh-keygen: To create my 4096-bit identity.

. openssl: For the heavy lifting of encryption.
. git: For version control and digital signing.
. ssh-agent: To manage my keys in the background.

--
🧠 Reflection: Why Linux?
A lot of people ask why we use Kali or Ubuntu instead of just Windows or Mac. For me, it comes down to two things:

Open Source: You can see exactly how the "engine" works.

The Toolbelt: Linux comes pre-loaded with specialized security tools that would take hours to configure on a standard OS. It’s built for the job.

--
🚀 Stretch Challenge: Key Fingerprints
I took it a step further by researching Key Fingerprints. By using the command to display a fingerprint, I learned how to verify I’m connecting to the right server before I even send my credentials. It’s the "ID check" of the internet.
