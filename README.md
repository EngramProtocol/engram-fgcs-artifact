# Engram Paper Artifact

This repository is the citable archival entry accompanying the manuscript:

> **Engram: Bitcoin-Anchored Data Publication and Persistent Decentralized
> Storage** — under review at *ACM Transactions on Internet Technology*
> (TOIT), 2026.

An earlier version of this manuscript was submitted to *Future Generation
Computer Systems* (FGCS) under the title "A Bitcoin-Anchored Modular
Architecture for Scalable Data Publication and Persistent Decentralized
Storage". The `v1.0.0-FGCS-evaluation` release tag corresponds to that
submission.

**DOI:** `10.5281/zenodo.19879674`

The work is developed at Hanoi University of Science and Technology with
A-Star Group and the University of Massachusetts Boston.

---

## Scope of this archive

The paper reports a bounded feasibility evaluation of the Engram protocol,
combining a geo-distributed prototype, a separate outage-resilience
deployment, a 500-node discrete-event simulation, and a historical workload
trace. The evidentiary status of each result is stated in the paper itself.
This repository exists to give that evaluation a stable, citable reference
point; it is not where the code lives.

## Where the code lives

The protocol and research track is developed in public under the
[Engram Protocol organization](https://github.com/EngramProtocol), Apache-2.0:

| Repository | What it is |
|---|---|
| [engram-anchor-bridge](https://github.com/EngramProtocol/engram-anchor-bridge) | Checkpoint anchoring bridge: reads finalized blocks, builds Merkle-batched commitments, submits them to the settlement backend |
| [engram-simulation-benchmark](https://github.com/EngramProtocol/engram-simulation-benchmark) | Evaluation suite reproducing the paper's measured results, with a table mapping each command to the result it produces |

Application-layer and internal infrastructure repositories are private.
Everything on the protocol and research track is public, and the roadmap for
what moves into public next (direct Bitcoin anchoring, an independent
verification library, a reference implementation of verifiable retrieval) is
described on the [organization profile](https://github.com/EngramProtocol).

## Reproducing the reported results

Start with `engram-simulation-benchmark`. Its README maps each module to the
section and table it produces, and states which modules run offline and which
need a testnet endpoint. If a number in the paper and a module's output
disagree, please open an issue on that repository rather than emailing; a
public correction is more useful than a private one.

## Data availability

The supporting data includes the historical occupancy trace behind the
settlement-cost analysis, the configuration parameters and random seeds for
the 500-node simulation, and the raw measurement logs from the prototype
experiments. Seeds and configuration are being migrated into
`engram-simulation-benchmark` so that the simulation results are reproducible
from the public repository alone. Until that migration is complete, the
remaining material is available on request; open an issue or contact the
corresponding author of the paper.

## Citation

If this work informs subsequent research, please cite the accompanying paper.
A BibTeX entry will be added on final publication.

## License

MIT. See `LICENSE`. Code repositories under the organization are Apache-2.0.
