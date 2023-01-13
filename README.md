# Azure DevOps Server supply chain attack tree v0.2.0 (! in DEV - important !)

# Introduction

Azure DevOps server supply-chain attack tree (map, Attack surface, threat modeling). The attack trees present in this repository were generated using the [Deciduous tool](https://www.deciduous.app).

# Content

- Introduction;
- Not considered;
- Attacker's goals;
- Attack tree;
- Useful links.

# Not considered

- Attacks aimed at elevating access rights to previously compromised accounts.

# Attacker's goals

I have identified the following possible targets for an attacker:
- **Leak source code** (or accidentally publish the code on some Internet resource by careless developer);
- **Submit malicious code**;
- **Modify release tag to point vulnerable commit** - the application is not being built from the expected commit (from the attacker's commit);
- **Delete malicious code from history (i.e. force push or delete branch)** - evidence clearing;
- **Remove a repository** - disrupt the development process;
- **RCE on ADO Server or Build agent** -> **Lateral movement** and other malicious activity -> **Submit malicious code**.

The attacker's targets in the attack tree are indicated by a purple rounded rectangle.

# Attack tree

![Azure DevOps Server supply chain attack tree](https://raw.githubusercontent.com/sergiomarotco/Azure-DevOps-server-supply-chain-attack-tree/2e2b93e7a88962b2586e5de390d448e242015e1f/assets/Source_Control_Management.svg)

# Useful links
- [GitHub supply chain attack tree](https://github.com/boostsecurityio/supply-chain-research) by [boostsecurityio](https://github.com/boostsecurityio).
