# 🌐 DNS (Domain Name System)

<div align="center">

![DNS Banner](https://img.shields.io/badge/Cybersecurity-DNS-blue?style=for-the-badge\&logo=cloudflare)
![Protocol](https://img.shields.io/badge/Protocol-Application%20Layer-green?style=for-the-badge)
![Port](https://img.shields.io/badge/Port-53-orange?style=for-the-badge)

### 📚 Cybersecurity Learning Journey

*"Understanding how the Internet translates names into addresses."*

</div>

---

## 🎯 What is DNS?

**DNS (Domain Name System)** is the Internet's naming service that translates human-readable domain names into machine-readable IP addresses.

Instead of remembering:

```text
142.250.193.78
```

We can simply use:

```text
google.com
```

DNS acts like the **phonebook of the Internet**, helping users and applications locate servers and services efficiently.

---

## 🏗️ DNS Basics

### 📌 Layer

DNS operates at the **Application Layer** of the TCP/IP model.

### 📌 Default Ports

| Protocol | Port |
| -------- | ---- |
| UDP      | 53   |
| TCP      | 53   |

✅ **UDP 53** is used for most DNS queries because it is faster.

✅ **TCP 53** is used as a fallback for larger responses and zone transfers.

---

## 🔄 How DNS Works

```text
User Types:
www.example.com

        │
        ▼

DNS Query Sent

        │
        ▼

DNS Resolver

        │
        ▼

DNS Server

        │
        ▼

IP Address Returned

        │
        ▼

Connect to Website
```

Example:

```text
example.com
        │
        ▼
192.168.1.10
```

DNS tells your device:

> "Go to the server located at this IP address."

---

# 📝 Common DNS Record Types

DNS records store information about domains and services.

---

## 🔹 A Record (Address Record)

Maps a hostname to an **IPv4 address**.

### Example

```text
example.com → 192.168.1.10
```

When someone visits:

```text
example.com
```

DNS responds:

```text
Go to 192.168.1.10
```

### Use Case

✅ Hosting websites on IPv4 servers

---

## 🔹 AAAA Record (Quad-A Record)

Maps a hostname to an **IPv6 address**.

### Example

```text
example.com
→
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

When someone visits:

```text
example.com
```

DNS responds:

```text
Go to this IPv6 address.
```

### Note

Many beginners think AAAA means:

```text
Authentication
Authorization
Accounting
```

❌ That's incorrect.

✅ AAAA simply refers to the IPv6 DNS record type and is pronounced **"Quad-A Record."**

### Use Case

✅ Websites using IPv6 networking

---

## 🔹 CNAME Record (Canonical Name)

Creates an alias from one domain name to another.

### Example

```text
www.example.com
        │
        ▼
example.com
```

DNS Records:

```text
A Record:
example.com → 192.168.1.10

CNAME:
www.example.com → example.com
```

### Why Use It?

Instead of managing multiple IP addresses:

```text
www.example.com
blog.example.com
shop.example.com
```

You can point them to one canonical domain.

### Use Case

✅ Domain aliases

✅ Subdomain redirection

---

## 🔹 MX Record (Mail Exchange Record)

Specifies which mail server receives emails for a domain.

### Example

```text
example.com
        │
        ▼
mail.example.com
```

When someone sends an email to:

```text
user@example.com
```

The sender's mail server checks the MX record and learns:

```text
Deliver mail to:
mail.example.com
```

---

## 📮 Easy Analogy

| Internet Service | Real World Example       |
| ---------------- | ------------------------ |
| Website          | 🏢 Office Building       |
| Email Address    | 📬 Mail Room             |
| DNS Record       | 📍 Building Address      |
| MX Record        | 📮 Mail Delivery Address |

DNS records help visitors find your office.

MX records help the postal service deliver your letters.

---

## 🛡️ Why DNS Matters in Cybersecurity

DNS is a critical component of cybersecurity because attackers often abuse it for:

* 🎣 Phishing attacks
* 🌍 Domain spoofing
* 🔍 Reconnaissance
* 🚨 Malware communication
* 📡 Command & Control (C2) traffic

Understanding DNS helps security professionals:

* Detect malicious domains
* Investigate incidents
* Analyze network traffic
* Improve threat detection

---

## 📚 Key Takeaways

✅ DNS translates domain names into IP addresses.

✅ DNS operates at the Application Layer.

✅ DNS primarily uses UDP Port 53.

✅ TCP Port 53 is used when necessary.

✅ A Records map domains to IPv4 addresses.

✅ AAAA Records map domains to IPv6 addresses.

✅ CNAME Records create aliases.

✅ MX Records define mail servers.

✅ DNS knowledge is essential for cybersecurity and network analysis.

---

### 🚀 Cybersecurity Journey

This note is part of my Cybersecurity Learning Journey where I document networking, security concepts, tools, and hands-on labs while building a strong foundation in cybersecurity.
