# Threats and Defenses of Backdoor Attacks in Machine Learning

**Authors:** Rohit Joshi and Turag Ikbal (University of Massachusetts Amherst)

This repository contains the research paper and corresponding LaTeX source code for our study on the landscape of backdoor attacks and defenses in machine learning.

**[➡️ View the Full Research Paper (PDF)](https://drive.google.com/file/d/1Kg4EjXJtlodbsPLTIkcdTLqTY3EsOfGj/view?usp=drive_link)**

---

## Abstract

Machine Learning (ML) has become a driving force behind many real-world technologies, from self-driving cars to financial modeling. [cite_start]However, this growing influence has introduced significant security challenges. [cite_start]This paper investigates the evolving threat of backdoor attacks, a form of training-time data poisoning where an adversary secretly plants a "trigger" into a model. [cite_start]When the model is deployed, it performs normally on standard inputs but will produce an attacker-chosen, malicious output whenever the trigger is present. [cite_start]These attacks are difficult to detect with standard validation tests because the trigger constitutes only a small fraction of the overall data. [cite_start]We explore the attack landscape, current defensive strategies, and real-world implications, particularly in federated learning environments. [cite_start]As there is currently no all-encompassing defense, this remains a critical open research problem.

---

## Key Findings & Topics Covered

This research provides a comprehensive overview of the backdoor attack ecosystem:

* **Attack Landscape**:
    * [cite_start]Backdoor attacks can be injected during centralized training by poisoning public datasets or through compromised clients in Federated Learning (FL).
    * [cite_start]**Static Triggers** are fixed patterns, like a specific pixel patch, that can achieve high attack success rates (ASR).
    * [cite_start]**Dynamic Triggers** are more advanced, changing their appearance with each input to evade simple filters while still achieving near-perfect ASR.
    * Attacks are classified by **label visibility**:
        * [cite_start]**Dirty-label attacks** modify both the input and its label (e.g., picture of a cat labeled as a dog).
        * [cite_start]**Clean-label attacks** keep the original label, making them harder to spot through manual inspection.

* **Defense Landscape**:
    * [cite_start]Defensive strategies are still evolving, with no single solution being universally effective.
    * [cite_start]**Data-centered filtering** aims to identify and remove poisoned data before training by looking for statistical anomalies.
    * [cite_start]**Model-centered purification** involves repairing an already-trained model, for example, through activation pruning or post-training purification (PBP).
    * [cite_start]**Robust training objectives** modify the learning process to make the model inherently more resistant to hidden triggers.
    * [cite_start]**Federated Learning safeguards**, like robust aggregation and frameworks such as FedDefender, are designed to mitigate attacks in decentralized environments where the server cannot inspect client data directly.

* **Real-World Implications in Federated Learning**:
    * [cite_start]Federated Learning is particularly vulnerable, as an attacker can compromise a small number of clients to inject a backdoor into the global model.
    * [cite_start]Case studies show that distributed backdoor attacks can achieve over 90% ASR with a minimal drop in clean accuracy.
    * [cite_start]Defenses like FedDefender have shown promise, drastically reducing the ASR from 90% to 7% in tested scenarios.

---

## How to Cite This Work

If you find this research useful in your own work, we encourage you to cite it. You can use the BibTeX entry below:

```bibtex
@misc{ikbal_joshi_2025_backdoor_threats,
  title        = {Threats and Defenses of Backdoor Attacks in Machine Learning},
  author       = {Ikbal, Turag and Joshi, Rohit},
  year         = {2025},
  publisher    = {GitHub},
  journal      = {GitHub repository},
  howpublished = {\url{[https://github.com/roheetyeet/backdoor-attacks-defenses-survey](https://github.com/roheetyeet/backdoor-attacks-defenses-survey)}}
}
```

---