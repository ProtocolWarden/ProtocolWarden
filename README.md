# ProtocolWarden

Contract-first AI operations ecosystem built around semantic repo graphs,
execution protocols, policy-controlled routing, and public-safe architecture
projection.

## What this repo is

The GitHub organization profile front door for the ProtocolWarden ecosystem — a
human-readable index of the component repos and links into the full
documentation site.

## What this repo is not

Not a code package and not the documentation source. There is no runtime,
library, or build artifact here. Canonical docs live at
[protocolwarden.github.io](https://protocolwarden.github.io/), and each
component lives in its own repo (catalogued below).

## Getting started

Start at the [documentation site](https://protocolwarden.github.io/), then use
the repo catalog below to jump into a specific component.

## What to click next

- Full documentation: **[protocolwarden.github.io](https://protocolwarden.github.io/)**
- Repo catalog: [protocolwarden.github.io/repos/](https://protocolwarden.github.io/repos/)
- Architecture charter: [protocolwarden.github.io/architecture/](https://protocolwarden.github.io/architecture/)
- Governance: [protocolwarden.github.io/governance/](https://protocolwarden.github.io/governance/)

## Architecture overview

```mermaid
graph TD
    DOCS["protocolwarden.github.io — full docs"]

    subgraph proto ["Protocol / Semantic layer"]
        RG[RepoGraph]
        PM[PlatformManifest]
        CX[CxRP]
        RX[RxP]
    end

    subgraph ctrl ["Control / Runtime layer"]
        OPS[OperationsCenter]
        SB[SwitchBoard]
        OC[OperatorConsole]
        ER[CoreRunner]
    end

    subgraph exec ["Execution Backend layer"]
        TE[TeamExecutor]
        DE[DAGExecutor]
        CE[CritiqueExecutor]
    end

    subgraph cog ["Cognition Lifecycle layer"]
        CLP[ContextLifecycle]
    end

    subgraph gov ["Governance / Lifecycle layer"]
        CU[Custodian]
        SR[SourceRegistry]
        PD[PlatformDeployment]
        WH[Warehouse]
        SM[SyncMechanism]
    end

    DOCS --> proto
    DOCS --> ctrl
    DOCS --> gov
    proto --> ctrl
    OPS --> TE
    OPS --> DE
    OPS --> CE
    OPS --> CLP
```

## Protocol / Semantic layer

| Repo | Role |
| --- | --- |
| [RepoGraph](https://github.com/ProtocolWarden/RepoGraph) | shared graph semantics, schema governance, boundary artifact language |
| [PlatformManifest](https://github.com/ProtocolWarden/PlatformManifest) | public-safe repo graph projection publisher |
| [CxRP](https://github.com/ProtocolWarden/CxRP) | contract execution routing protocol — schemas and vocabulary |
| [RxP](https://github.com/ProtocolWarden/RxP) | runtime execution protocol — invocation and result contracts |

## Control / Runtime layer

| Repo | Role |
| --- | --- |
| [OperationsCenter](https://github.com/ProtocolWarden/OperationsCenter) | planning, routing, execution dispatch, policy, evidence, run artifacts |
| [SwitchBoard](https://github.com/ProtocolWarden/SwitchBoard) | policy-driven execution-lane and backend selector |
| [OperatorConsole](https://github.com/ProtocolWarden/OperatorConsole) | operator entrypoint — persistent workspaces, context continuity, delegation |
| [CoreRunner](https://github.com/ProtocolWarden/CoreRunner) | runtime invocation mechanics consuming RxP contracts |

## Execution Backend Layer

| Repo | Role |
| --- | --- |
| [TeamExecutor](https://github.com/ProtocolWarden/TeamExecutor) | coordinator/worker/verifier team execution — replaces kodo |
| [DAGExecutor](https://github.com/ProtocolWarden/DAGExecutor) | DAG workflow executor (rustworkx) — replaces Archon |
| [CritiqueExecutor](https://github.com/ProtocolWarden/CritiqueExecutor) | adversarial and reflexion critique loops — new capability |

## Cognition Lifecycle layer

| Repo | Role |
| --- | --- |
| [ContextLifecycle](https://github.com/ProtocolWarden/ContextLifecycle) | cognition lifecycle runtime — bounded, resumable agent sessions + context-injection tiered memory |

## Governance / Lifecycle layer

| Repo | Role |
| --- | --- |
| [Custodian](https://github.com/ProtocolWarden/Custodian) | cross-repo boundary, drift, and audit enforcement |
| [SourceRegistry](https://github.com/ProtocolWarden/SourceRegistry) | source and fork tracking and lifecycle |
| [PlatformDeployment](https://github.com/ProtocolWarden/PlatformDeployment) | local developer platform for the shared AI coding stack |
| [Warehouse](https://github.com/ProtocolWarden/Warehouse) | LLM-ready context packaging and staging |
| [SyncMechanism](https://github.com/ProtocolWarden/SyncMechanism) | public-safe Syncthing install + runtime mechanism (version pinning, tray, sync-spec validation) |

## Forks and External Integrations

Third-party forks (`openclaw`, `firecrawl`, `PraisonAI`, etc.) and retired integrations
(`kodo` → replaced by TeamExecutor, `Archon` → replaced by DAGExecutor) are documented at
[protocolwarden.github.io/repos/external-integrations/](https://protocolwarden.github.io/repos/external-integrations/).

## Public surface

| Repo | Purpose |
| --- | --- |
| [ProtocolWarden/ProtocolWarden](https://github.com/ProtocolWarden/ProtocolWarden) | this repo — GitHub profile front door |
| [ProtocolWarden/ProtocolWarden.github.io](https://github.com/ProtocolWarden/ProtocolWarden.github.io) | full documentation site |
