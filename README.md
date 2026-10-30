<div align="center">

```text
adil@systems:~$ whoami
Adil Alperen Ciftci :: systems security engineer
runtime boundaries | workload identity | protocol invariants | upstream engineering
```

# Adil Alperen Ciftci

**Systems Security Engineer** working where kernels, identity, cryptographic protocols, and production control planes meet.

[![Profile](https://img.shields.io/badge/GitHub-adilalperenciftci-0b1220?style=for-the-badge&logo=github&logoColor=22d3ee)](https://github.com/adilalperenciftci)
[![Linux](https://img.shields.io/badge/Linux-runtime%20security-0b1220?style=for-the-badge&logo=linux&logoColor=f59e0b)](https://www.kernel.org/)
[![eBPF](https://img.shields.io/badge/eBPF-telemetry-0b1220?style=for-the-badge&logoColor=22d3ee)](https://ebpf.io/)
[![Go](https://img.shields.io/badge/Go-control%20planes-0b1220?style=for-the-badge&logo=go&logoColor=22d3ee)](https://go.dev/)
[![Rust](https://img.shields.io/badge/Rust-runtime%20invariants-0b1220?style=for-the-badge&logo=rust&logoColor=f59e0b)](https://www.rust-lang.org/)

</div>

## Engineering map

| Boundary | Architecture focus | Representative systems |
| --- | --- | --- |
| **Linux/eBPF and kernel sandboxing** | cgroup-scoped execution evidence, datapath state machines, file-descriptor lifetime, capability reduction, Capsicum confinement | Cilium, Falco, Kata Containers, Linux, FreeBSD |
| **Workload identity and cryptographic protocols** | SPIFFE identities, X.509 path validation, RFC 5280 constraints, CA rotation, PKINIT trust boundaries | SPIRE, workload PKI, certificate toolchains |
| **Windows AD/Kerberos identity boundaries** | PAC semantics, delegated managed service accounts, graph-derived authorization edges, DNS name compression invariants | Impacket, BloodHound, SharpHound |
| **WAF and protocol invariant verification** | SecLang state, bounded parsers, checksum coverage, CoAP block transfer, TLS negotiation | Coraza, OWASP CRS, Scapy, libcoap, Nmap |

## Verified upstream merges

These links point to merged changes in the upstream repositories.

| Project | Merged engineering change |
| --- | --- |
| [Cilium #49130](https://github.com/cilium/cilium/pull/49130) | Applied `BackendTLSPolicy` validation and transport settings to Gateway API `GRPCRoute` backends. |
| [Falco libs #3112](https://github.com/falcosecurity/libs/pull/3112) | Preserved plugin field-extraction failures as observable runtime errors instead of losing the diagnostic boundary. |
| [SPIFFE/SPIRE #7303](https://github.com/spiffe/spire/pull/7303) | Capped CA rotation and issued X.509 lifetimes against the verified upstream chain expiry. |
| [Impacket #2304](https://github.com/fortra/impacket/pull/2304) | Bounded DNS compressed-name traversal when pointers form a cycle. |
| [DefectDojo #15961](https://github.com/DefectDojo/django-DefectDojo/pull/15961) | Corrected Finding Group visibility for authorized product members, including empty groups. |
| [Dependency-Track #7323](https://github.com/DependencyTrack/dependency-track/pull/7323) | Added optional HMAC-SHA256 authentication over the exact transmitted webhook bytes. |
| [Aether #3423](https://github.com/aether-lang-dev/aether/pull/3423) | Enforced certificate path length and issuer-validity constraints. |
| [Aether #3340](https://github.com/aether-lang-dev/aether/pull/3340) | Required `basicConstraints.cA` and `keyCertSign` during certificate path verification. |

## Current patch tracks

| System | Invariant under review |
| --- | --- |
| [Kata Containers #13933](https://github.com/kata-containers/kata-containers/pull/13933) | Preserve approved environment-variable bytes after validation. |
| [Coraza #1770](https://github.com/corazawaf/coraza/pull/1770) | Enforce non-file request-body accounting across multipart and partial-processing paths. |
| [OWASP CRS #4853](https://github.com/coreruleset/coreruleset/pull/4853) | Keep SQL token boundaries deterministic around `MEMBER OF` and `JSON_EXTRACT`. |
| [Scapy #5191](https://github.com/secdev/scapy/pull/5191) | Include encapsulated payload padding in UDP checksum coverage. |
| [Nmap #3584](https://github.com/nmap/nmap/pull/3584) | Offer SHA-384 signature schemes in the default NSE TLS negotiation set. |
| [RT-Thread #11935](https://github.com/RT-Thread/rt-thread/pull/11935) | Validate descriptor bounds and detach signal listeners safely during close. |
| [libcoap #2208](https://github.com/obgm/libcoap/pull/2208) | Preserve Block1 byte coverage when the block size exponent changes. |
| [Aether #3441](https://github.com/aether-lang-dev/aether/pull/3441) / [#3458](https://github.com/aether-lang-dev/aether/pull/3458) | Intersect independent sandbox policies and restore nested host map context. |

## Research and lab work

- [Runtime Provenance Firewall](https://github.com/adilalperenciftci/runtime-provenance-firewall): correlates cgroup-scoped eBPF evidence, artifact digests, SLSA provenance, and in-toto runtime statements; missing evidence blocks an allow decision.
- [Enterprise Purple Range](https://github.com/adilalperenciftci/enterprise-purple-range): isolated Windows identity, endpoint, and network evidence correlation lab.
- [Adversary Validation Range](https://github.com/adilalperenciftci/adversary-validation-range): controlled validation actions against disposable targets with benign baselines and detection assertions.
- [CPS Process-Integrity Harness](https://github.com/adilalperenciftci/cps-adversary-emulation-harness): deterministic synthetic process-integrity experiments without physical-controller interaction.

## Verification discipline

```text
issue state -> minimal reproducer -> BEFORE failure -> root cause
           -> surgical patch -> AFTER pass -> related-package regression
```

Builds and runtime tests execute in isolated lab environments. Patch scope stays narrow, state-machine assumptions are made explicit, and every public result states what was verified and what remains platform-dependent.

## Activity

<div align="center">
  <img width="49%" alt="GitHub statistics" src="https://github-readme-stats.vercel.app/api?username=adilalperenciftci&show_icons=true&hide_border=true&theme=transparent&title_color=22d3ee&text_color=cbd5e1&icon_color=f59e0b" />
  <img width="49%" alt="Most used languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=adilalperenciftci&layout=compact&hide_border=true&theme=transparent&title_color=22d3ee&text_color=cbd5e1" />
</div>

<div align="center">
  <img width="98%" alt="Contribution activity graph" src="https://github-readme-activity-graph.vercel.app/graph?username=adilalperenciftci&bg_color=00000000&color=22d3ee&line=f59e0b&point=e2e8f0&area=true&hide_border=true" />
</div>

## Contact and cryptographic identity

Use [GitHub](https://github.com/adilalperenciftci) for project-specific engineering correspondence. No OpenPGP public key is currently published on this account; do not trust a third-party key as mine without an independently verified fingerprint.
