# Threats and Defenses of Backdoor Attacks in Machine Learning

**Authors:** Rohit Joshi and Turag Ikbal (University of Massachusetts Amherst)

This repository contains the research paper and corresponding LaTeX source code for our study on the landscape of backdoor attacks and defenses in machine learning.

**[➡️ View the Full Research Paper (PDF)](https://drive.google.com/file/d/1Kg4EjXJtlodbsPLTIkcdTLqTY3EsOfGj/view?usp=drive_link)**

**[➡️ View the Paper on ResearchGate](https://www.researchgate.net/publication/393019183_Threats_and_Defenses_of_Backdoor_Attacks_in_Machine_Learning)**

- DOI: 10.13140/RG.2.2.31657.10085

---

## Abstract

Machine Learning (ML) has become a driving force behind many real-world technologies, from self-driving cars to financial modeling. However, this growing influence has introduced significant security challenges. This paper investigates the evolving threat of backdoor attacks, a form of training-time data poisoning where an adversary secretly plants a "trigger" into a model. When the model is deployed, it performs normally on standard inputs but will produce an attacker-chosen, malicious output whenever the trigger is present. These attacks are difficult to detect with standard validation tests because the trigger constitutes only a small fraction of the overall data. We explore the attack landscape, current defensive strategies, and real-world implications, particularly in federated learning environments. As there is currently no all-encompassing defense, this remains a critical open research problem.

---

## Key Findings & Topics Covered

This research provides a comprehensive overview of the backdoor attack ecosystem:

* **Attack Landscape**:
    * Backdoor attacks can be injected during centralized training by poisoning public datasets or through compromised clients in Federated Learning (FL).
    * **Static Triggers** are fixed patterns, like a specific pixel patch, that can achieve high attack success rates (ASR).
    * **Dynamic Triggers** are more advanced, changing their appearance with each input to evade simple filters while still achieving near-perfect ASR.
    * Attacks are classified by **label visibility**:
        * **Dirty-label attacks** modify both the input and its label (e.g., picture of a cat labeled as a dog).
        * **Clean-label attacks** keep the original label, making them harder to spot through manual inspection.

* **Defense Landscape**:
    * Defensive strategies are still evolving, with no single solution being universally effective.
    * **Data-centered filtering** aims to identify and remove poisoned data before training by looking for statistical anomalies.
    * **Model-centered purification** involves repairing an already-trained model, for example, through activation pruning or post-training purification (PBP).
    * **Robust training objectives** modify the learning process to make the model inherently more resistant to hidden triggers.
    * **Federated Learning safeguards**, like robust aggregation and frameworks such as FedDefender, are designed to mitigate attacks in decentralized environments where the server cannot inspect client data directly.

* **Real-World Implications in Federated Learning**:
    * Federated Learning is particularly vulnerable, as an attacker can compromise a small number of clients to inject a backdoor into the global model.
    * Case studies show that distributed backdoor attacks can achieve over 90% ASR with a minimal drop in clean accuracy.
    * Defenses like FedDefender have shown promise, drastically reducing the ASR from 90% to 7% in tested scenarios.

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
