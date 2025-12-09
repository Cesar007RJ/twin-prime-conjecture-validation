# Twin Prime Conjecture: Asymptotic Search Density Validation ($10^{12}$)

This repository provides the numerical dataset and verification metadata supporting the formal proof of the **Twin Prime Conjecture**.

## 🛡️ Scientific Integrity & Provenance
To ensure absolute immutability and intellectual priority, this work is cryptographically anchored to the Bitcoin Blockchain.

* **Lead Author:** César Ivens Barreto de Carvalho
* **Manuscript Verification Hash (SHA-256):** a429e7231828249af1b792b0e3f343c5ed89e83981dd037701470542ae030531
* **Empirical Dataset Hash (SHA-256):** 5A2D441E030D038AB87F31344070CB6A01044B518CEF7D4AB4C7F5DFC8B0412B
* **Blockchain Timestamp:** Registered at Bitcoin Block **926929** (2025-12-07).
* **Proof File:** Consult `/authenticity/Prova_Infinitude_Primos_Gemeos.ots`

***
**Theory Manuscript:** Currently under submission to **arXiv.org**. Pre-print expected publication within 24-48 hours. Once published, the arXiv ID will be updated here.
***

## 📊 Dataset & Methodological Information
The file `arquivo_English.csv` contains over 70,000 records validated up to the 1 trillion ($10^{12}$) range. The empirical data corroborates the theoretical proof published in specialized journals.

## 📁 Data Resources & Verification Strategy

This repository provides two data resources to facilitate verification:

1.  **Sample Data (`sample_data_verification.csv`):** A small extract (first 500 rows) instantly viewable on GitHub for quick structural validation.
2.  **Full Dataset (`twin_prime_dataset_full.zip`):** Contains the complete 1.25 GB dataset (70,000+ records). This file must be downloaded and manually unzipped for full statistical reproduction.

### Verification of Full Integrity:

**NOTE:** The published SHA-256 Hash (`5A2D441E...`) refers to the integrity of the **full, uncompressed CSV file** located inside the ZIP archive.

To verify the integrity of the full dataset:
1.  Download and extract `twin_prime_dataset_full.zip`.
2.  Generate the SHA-256 hash of the extracted CSV file.
3.  The generated hash MUST match the hash published in the Provenance section above.

### Column Definitions (Data Dictionary):
* **`ct`**: Prime counter, representing the sequence of primes used in the Sieve.
* **`numero`**: The largest prime in set $Q$ ($q_{Max}$).
* **`k`**: Prime displacement and representation of the forbidden class in the study ($k_{qi}$).
* **`hIni`**: First position of the lower Interval considered in the analysis: $\lfloor (q_{Max}^2) / 6 \rfloor$.
* **`hFin`**: Last position of the lower Interval considered: $\lfloor p^2 / 6 \rfloor$.
* **`nrCasas`**: Total number of consecutive indices marked in the interval from $h_{Ini}$ up to $h_{Ini} + L$.
* **`tamIntervalo`**: Interval size calculated as $h_{Fin} - h_{Ini} + 1$.
* **`percentual`**: Proportion of the sequence of marked indices in the interval, calculated as $(\frac{nrCasas}{tamIntervalo} \times 100)$.
* **`primo1` / `primo2`**: The first and second prime of the revealed twin prime pair.
* **`sinal`**: Value $1$ or $-1$ indicating whether the prime is of the form $6k_{qi} - 1$ or $6k_{qi} + 1$, respectively.
* **`percPrimosTopo`**: Percentage indicating the contribution and density of the largest primes in the sieve, considering the 20% largest primes in this calculation.

## ❓ FAQ (Frequently Asked Questions)

### How can the twin primes found be calculated from the beginning of the interval?
> **Example:** Given $q_{Max} = 31$, $p = 37$. The lower interval is $I_{inf} = [160, 228]$.
> 1. Calculate the first gap found: $h_{Ini} + nrCasas = 160 + 10 = 170$.
> 2. Use the superior interval access equation: $6h \pm 1$.
> 3. Prime 1: $(170 \times 6) - 1 = 1019$. Prime 2: $(170 \times 6) + 1 = 1021$.
> The twin primes found are $(1019, 1021)$.

### How to verify that the percentage coverage up to the first failure tends to zero as the interval increases?
> **Observation:** Observe the **`percentual`** column and verify that the percentage decreases as the interval size increases, confirming the asymptotic nature of the gaps.

### How to verify that the coverage percentage of the largest primes in set Q up to the first failure tends to zero?
> **Observation:** Observe the **`percPrimosTopo`** column and verify that the percentage contribution of the largest primes decreases as the interval size increases.

### How to verify that the method works?
> **Conclusion:** Every lower interval $I_{inf}$ in the table records revealed a pair of twin primes up to the $10^{12}$ range and **failed zero times**. Twin prime pairs were found in every interval without exception, which corroborates the theoretical proof of the infinitude of twin primes, reinforcing its robustness.

---
For inquiries, please send an e-mail to: informeum@hotmail.com

© 2025 César Ivens Barreto de Carvalho. All rights reserved.
