# 🌌 Nebula Level 06 
Progetto svolto durante il corso di 'Programmazione Sicura' a.a. 2024/2025
> Analisi, sfruttamento e mitigazione della vulnerabilità del livello 06 di Nebula (https://exploit.education/nebula/level-06/).

---

## Panoramica

Il livello 06 di *Nebula* presenta un sistema vulnerabile in cui le credenziali vengono memorizzate utilizzando un **algoritmo di hash obsoleto**.

L’obiettivo è ottenere l’accesso all’utente `flag06`, sfruttando la debolezza dell’hash e configurazioni errate del sistema.

---

## Analisi della vulnerabilità

- **Tipo di vulnerabilità:**  
  Weak Password Hashing, Weak Password Requirements

- **Componente vulnerabile:**  
  Uso dell’algoritmo **NBS DES** (via `crypt()`), con hash salvato in chiaro nel file `/etc/passwd`

---


##  Strumenti utilizzati
- **John the Ripper** — per il cracking dell’hash di `flag06`  


## 🚩Ottenimento bandierina

Il superamento del livello avviene sfruttando la **debolezza dell’algoritmo NBS DES** utilizzato per l’hash della password.  
Una volta recuperata la password di `flag06`, è possibile ottenere la bandierina eseguendo il comando `getflag` con i privilegi dell’utente target.

---

### Autori
  - Daniele Dello Russo (https://github.com/Presidente10)
  - Mario Lezzi (https://github.com/MarioLezzi92)
