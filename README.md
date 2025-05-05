# 🌌 Nebula Level 06 
Progetto svolto durante il corso di 'Programmazione Sicura' a.a. 2024/2025
> Analisi, sfruttamento e mitigazione della vulnerabilità del livello 06 della macchina virtuale Nebula : [https://exploit.education/nebula/](https://exploit.education/nebula/level-06/).

---

## 🧭 Panoramica

Il livello 06 di *Nebula* presenta un sistema vulnerabile in cui un utente (level06) può accedere alla home di un utente privilegiato (flag06), e leggere file `/etc/passwd` contenente l'hash della password.

L’obiettivo è ottenere le credenziali di `flag06` sfruttando configurazioni errate o hash deboli.

---

## 🔍 Analisi della vulnerabilità

- **Tipo di vulnerabilità:**  
  Weak password hashing & Weak Password Requirements

- **Componente vulnerabile:**  
  Uso dell’algoritmo NBS DES (via `crypt()`), storage dell’hash in `/etc/passwd`

---


## 🧑‍💻 Software utilizzati
  Utilizzo di John the Ripper per il cracking della password 


## 🚩 Ottenimento bandierina

Il superamento del livello avviene sfruttando l'algoritmo di cifratura datato utilizzato per lo storage della password

