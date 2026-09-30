# Adil Alperen Çiftci

**Systems security & security engineering** · runtime security · workload identity/PKI · software supply chain

I work on trust boundaries where build provenance, runtime evidence, and identity meet. My projects favor explicit scope, deterministic verification, and fail-closed decisions when evidence is missing or inconsistent.

## Selected upstream contributions

| Project | Engineering change | Status |
| --- | --- | --- |
| [SPIFFE / SPIRE](https://github.com/spiffe/spire/pull/7303) | Use verified upstream X.509 chain expiry when rotating CAs and capping issued SVID lifetimes. | Merged |
| [Dependency-Track](https://github.com/DependencyTrack/dependency-track/pull/7323) | Sign outgoing webhook payloads with optional HMAC-SHA256 over the transmitted bytes. | Merged |
| [DefectDojo](https://github.com/DefectDojo/django-DefectDojo/pull/15961) | Correct Finding Group visibility for authorized product members, including empty groups. | Merged |

## Selected security research

| Project | Boundary and evidence |
| --- | --- |
| [Runtime Provenance Firewall](https://github.com/adilalperenciftci/runtime-provenance-firewall) | Research prototype joining cgroup-scoped Linux/eBPF execution evidence, artifact digests, SLSA provenance, and in-toto Runtime Trace statements; known event loss blocks `ALLOW`. |
| [Agent Boundary](https://github.com/adilalperenciftci/agent-boundary) | Local policy decisions for bounded agent tool calls, with strict normalization and a redacted evidence ledger. An `allow` decision is not proof of safety. |
| [Adversary Validation Range](https://github.com/adilalperenciftci/adversary-validation-range) | Controlled actions against disposable targets → captured evidence → detection checks against attack and benign baselines. |
| [Enterprise Purple Range](https://github.com/adilalperenciftci/enterprise-purple-range) | Isolated enterprise lab correlating Windows endpoint, identity, and network evidence; unfinished experiments remain `NOT_TESTED`. |
| [CPS Adversary-Emulation Harness](https://github.com/adilalperenciftci/cps-adversary-emulation-harness) | Deterministic, synthetic OT/process-integrity experiments for detector regression; the socketless emulator does not interact with physical controllers. |

## Engineering focus

Linux/eBPF telemetry, workload identity and PKI, supply-chain provenance, detection engineering, and security-critical systems correctness. Tests and threat models in the linked repositories state what each result establishes and where its trust boundary ends.

Security experiments are limited to project-owned fixtures, isolated labs, or explicitly authorized systems.
