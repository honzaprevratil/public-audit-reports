# Public Audit Reports

Smart contract security audits I worked on as an **auditor** or **lead auditor** at
[Ackee Blockchain Security](https://ackee.xyz). Only reports that have been made public are listed here.

Each audit links to:

- the **project** itself (website, docs, code), where it still exists,
- the **original report** as published by the client,
- the **Ackee report** in [Ackee-Blockchain/public-audit-reports](https://github.com/Ackee-Blockchain/public-audit-reports),
- a **backup copy** stored in this repository in [`pdf/`](pdf/).

## Overview

| Project | Scope | My role | Audit period | Findings | Reports |
| --- | --- | --- | --- | :---: | --- |
| [Let's get HAI](#lets-get-hai-new-core-features) | New Core Features | Lead Auditor | Mar 2025 | 25 | [Original][hai-orig] · [Ackee][hai-ackee] · [Backup][hai-backup] |
| [Cian](#cian-yield-layer) | Yield Layer | Auditor | Nov – Dec 2024 | 26 | [Original][cian-orig] · [Ackee][cian-ackee] · [Backup][cian-backup] |
| [Axelar](#axelar-interchain-token-service) | Interchain Token Service | Auditor | Oct – Nov 2024 | 17 | [Original][axelar-orig] · Ackee ¹ · [Backup][axelar-backup] |
| [Rhinestone](#rhinestone-core-modules) | Core Modules | Auditor | Apr – Sep 2024 | 36 | [Original][rhinestone-orig] · [Ackee][rhinestone-ackee] · [Backup][rhinestone-backup] |

¹ Not published in the Ackee repository, see [Axelar](#axelar-interchain-token-service).

### Findings by severity

| Project | Critical | High | Medium | Low | Warning | Info | **Total** |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Let's get HAI: New Core Features | 2 | 2 | 4 | 3 | 4 | 10 | **25** |
| Cian: Yield Layer | 0 | 0 | 3 | 4 | 9 | 10 | **26** |
| Axelar: Interchain Token Service | 0 | 0 | 1 | 3 | 5 | 8 | **17** |
| Rhinestone: Core Modules | 0 | 7 | 4 | 6 | 10 | 9 | **36** |

---

## Audits

### Let's get HAI: New Core Features

HAI is a GEB-fork stablecoin protocol on Optimism that mints the HAI stablecoin against multiple
collateral types. The audit covered the newly added features: KITE staking and rewards,
Merkle-tree based daily reward distribution, the haiVELO wrapper for Velodrome, and Beefy / Yearn
Velo vault oracles.

| | |
| --- | --- |
| **Role** | Lead Auditor (together with Dmytro Khimchenko) |
| **Period** | Mar 4 – Mar 14, 2025 (10 engineering days), fix reviews in April 2025 |
| **Final report** | Revision 2.0, Apr 25, 2025 |
| **Project** | [letsgethai.com](https://www.letsgethai.com) · [Docs](https://docs.letsgethai.com) · [GitHub](https://github.com/hai-on-op/core) |
| **Original report** | [hai-on-op/audit-reports][hai-orig] (revision 1.1) |
| **Ackee report** | [Ackee-Blockchain/public-audit-reports][hai-ackee] (revision 2.0) |
| **Backup** | [`pdf/ackee-blockchain-let's-get-hai-new-core-features-report.pdf`][hai-backup] (revision 2.0) |

### Cian: Yield Layer

Cian is a yield protocol where users deposit assets into vaults and the Yield Layer allocates them
to yield-generating strategies. The audit covered all Yield Layer contracts (vaults, redemption
and fee logic, exchange price updates), excluding the strategies themselves, and included
dedicated fuzzing.

| | |
| --- | --- |
| **Role** | Auditor (lead auditor: Jan Kalivoda) |
| **Period** | Nov 27 – Dec 11, 2024 (15 engineering days), fix review in December 2024 |
| **Final report** | Revision 1.1, Jan 14, 2025 |
| **Project** | [cian.app](https://cian.app) · [Yield Layer docs](https://docs.cian.app/yieldlayer) |
| **Original report** | [docs.cian.app → Audit Report][cian-orig] |
| **Ackee report** | [Ackee-Blockchain/public-audit-reports][cian-ackee] |
| **Backup** | [`pdf/ackee-blockchain-cian-yield-layer-report.pdf`][cian-backup] |

### Axelar: Interchain Token Service

Axelar's Interchain Token Service (ITS) is a cross-chain token bridging protocol built on the
Axelar Network. It lets tokens move between chains via token managers (lock/unlock or mint/burn)
while keeping consistent token properties. This audit focused on the newly introduced ITS Hub
integration.

| | |
| --- | --- |
| **Role** | Auditor (lead auditor: Lukáš Rajnoha) |
| **Period** | Oct 29 – Nov 29, 2024 (18 engineering days), fix review in January 2025 |
| **Final report** | Revision 1.1, Jan 16, 2025 |
| **Project** | [axelar.network](https://www.axelar.network) · [ITS portal](https://interchain.axelar.dev) · [GitHub](https://github.com/axelarnetwork/interchain-token-service) |
| **Original report** | [axelarnetwork/audits][axelar-orig] |
| **Ackee report** | Not published. The ITS report in the Ackee repository is an earlier, separate engagement (April 2024). |
| **Backup** | [`pdf/ackee-blockchain-axelar-its.pdf`][axelar-backup] |

### Rhinestone: Core Modules

Rhinestone builds modular smart account infrastructure based on ERC-7579. Core Modules are its
reference set of validators, executors and hooks (e.g. OwnableValidator, SocialRecovery,
MultiFactor, DeadManSwitch, ColdStorageHook, AutoSavings, ScheduledOrders), originally developed
as ModuleKit examples. The audit was done in two rounds: the initial review and a follow-up review
of the Uniswap integration changes.

| | |
| --- | --- |
| **Role** | Auditor (lead auditor: Štěpán Šonský) |
| **Period** | Apr 29 – May 24, 2024 (21 engineering days) and Sep 16 – 19, 2024 (2 engineering days) |
| **Final report** | Revision 2.1, Oct 3, 2024 |
| **Project** | [rhinestone.dev](https://www.rhinestone.dev) · [GitHub](https://github.com/rhinestonewtf/core-modules) |
| **Original report** | [rhinestonewtf/core-modules][rhinestone-orig] |
| **Ackee report** | [Ackee-Blockchain/public-audit-reports][rhinestone-ackee] |
| **Backup** | [`pdf/ackee-blockchain-rhinestone-core-modules-report.pdf`][rhinestone-backup] |

---

## Backup copies (`pdf/`)

The [`pdf/`](pdf/) folder is a **backup**. It keeps a copy of every report in case the original
links stop working (repositories get moved, docs get rebuilt, files get removed). The links above
always point to the published sources first.

The backups are byte-identical to the published reports:

| File | SHA-256 |
| --- | --- |
| `ackee-blockchain-let's-get-hai-new-core-features-report.pdf` | `26f80ece5957a49aa8f5febc60b8131f07d4c391cad10036bb5c956084cd0628` |
| `ackee-blockchain-cian-yield-layer-report.pdf` | `81b597ce33ed7f894e5f9bf9c04c05d3f4dad52f7be0be93f5a5071da9908740` |
| `ackee-blockchain-axelar-its.pdf` | `4108ef6096c55aee7a41f40c732a882909f153a77efce25c614e71002862a959` |
| `ackee-blockchain-rhinestone-core-modules-report.pdf` | `a94840d327f9582058417203a2624fc5251d3cbcbccfee52b72c62e3e87baf74` |

To check a local copy:

```bash
shasum -a 256 pdf/*.pdf
```

Ackee also publishes a `.pdf.sig` signature next to each report in its repository, which can be
used to verify authenticity.

## Disclaimer

All reports were authored by Ackee Blockchain Security for the respective clients and are shared
here unchanged, for reference only. An audit reflects the code at the audited commits and is not a
guarantee that the code is free of vulnerabilities. Nothing here is investment advice.

<!-- Report links -->
[hai-orig]: https://github.com/hai-on-op/audit-reports/blob/main/ackee_HAI_new-core-features_report.pdf
[hai-ackee]: https://github.com/Ackee-Blockchain/public-audit-reports/blob/master/2025/ackee-blockchain-let%27s-get-hai-new-core-features-report.pdf
[hai-backup]: pdf/ackee-blockchain-let%27s-get-hai-new-core-features-report.pdf
[cian-orig]: https://docs.cian.app/security-and-risk/audit-report#yield-layer-audit-report-ackee
[cian-ackee]: https://github.com/Ackee-Blockchain/public-audit-reports/blob/master/2025/ackee-blockchain-cian-yield-layer-report.pdf
[cian-backup]: pdf/ackee-blockchain-cian-yield-layer-report.pdf
[axelar-orig]: https://github.com/axelarnetwork/audits/blob/main/audits/2025-01%20Ackee_ITS.pdf
[axelar-backup]: pdf/ackee-blockchain-axelar-its.pdf
[rhinestone-orig]: https://github.com/rhinestonewtf/core-modules/blob/main/audits/ackee-blockchain-rhinestone-core-modules-report.pdf
[rhinestone-ackee]: https://github.com/Ackee-Blockchain/public-audit-reports/blob/master/2024/ackee-blockchain-rhinestone-core-modules-report.pdf
[rhinestone-backup]: pdf/ackee-blockchain-rhinestone-core-modules-report.pdf
