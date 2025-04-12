# Awesome CTV+CSFS

A curated list of resources, tools, and projects related to OP_CHECKTEMPLATEVERIFY (CTV) and OP_CHECKSIGFROMSTACK (CSFS) in Bitcoin.

## Quick Start: Run CTV+CSFS Signet

Want to experiment with CTV and CSFS right away? Run your own signet node with both opcodes enabled:

```bash
git clone https://github.com/arshbot/ctv-csfs-signet-docker
cd ctv-csfs-signet-docker
cp .env.example .env
docker-compose up -d
```

This will start a Bitcoin signet node with both CTV and CSFS enabled, perfect for development and testing. See the [CTV+CSFS Signet Node](#ctv-csfs-signet-node) tool below for more details.

## Table of Contents
- [Projects](#projects)
- [Tools](#tools)
- [Learning Resources](#learning-resources)
- [Community Discussions](#community-discussions)
- [Contributing](#contributing)

## Projects

A collection of interesting projects utilizing covenants, particularly focusing on CTV+CSFS implementations.

| Name | Links | Description | Phase | CTV | CSFS | TXHASH | CAT | CCV |
|------|-------|-------------|-------|-----|------|--------|-----|-----|
| Pool | [Slides](https://notes.dunst.be/slide/#/2/slide/view/Ekky-cAegV9dSOaNOjH9TStNOmAnrhDDc9hxHlmRs5M/embed/present/),<br>[Code](https://github.com/stutxo/op_ctv_payment_pool),<br>[Sapio](https://github.com/sapio-lang/sapio/tree/master/plugin-example/payment_pool),<br>[Article](https://rubin.io/bitcoin/2021/12/15/advent-18/),<br>[Intro](https://rubin.io/bitcoin/2021/12/10/advent-13/),<br>[IRC](https://freenode.irclog.whitequark.org/bitcoin-wizards/2019-05-21#24639752),<br>[Coinpools](https://discrete-blog.github.io/coinpool/) | Scalable payment pool with CTV - supports up to 21 users, P2A fee management, and automatic coinjoin-like privacy | Prototype | ✓ | | | | |
| Vault | [CTV Vault](https://github.com/jamesob/simple-ctv-vault),<br>[Demo](https://github.com/jamesob/opvault-demo),<br>[Sandwich](https://github.com/stutxo/Op_SecureTheSandwich) | Vault without pre-signed transactions | Prototype | ✓ | | | | |
| Matt Vault | [Code](https://github.com/bitcoin-inquisition/bitcoin/compare/24.0...bigspider:bitcoin-inquisition:matt-vault) | Vault implementation using CTV and contract verification opcodes | Prototype | ✓ | | | | ✓ |
| Android CTV Demo | [Code](https://github.com/percy-g2/android_app_ctv_playground),<br>[Release](https://github.com/percy-g2/android_app_ctv_playground/releases/tag/v0.1.0) | Native Android implementation demonstrating CTV Vault and payment pools with interactive UI | Prototype | ✓ | | | | |
| DLCs | [Specs](https://github.com/discreetlogcontracts/dlcspecs/),<br>[Cases](https://covenants.info/use-cases/dlcs/),<br>[DLCAT](https://github.com/bennyhodl/dlcat) | 30x more performant DLCs | Prototype / Spec | ✓ | | ✓ | | ✓ |
| Ark | [Bark](https://codeberg.org/ark-bitcoin/bark/commits/branch/ctv) | Layer 2 protocol | Prototype | ✓ | | ✓ | | |
| BitVM | [Thread](https://delvingbitcoin.org/t/how-ctv-csfs-improves-bitvm-bridges/1591) | Trust-minimized Bitcoin interoperability | Prototype | ✓ | ✓ | | ✓ | |
| Simple CTV | [Code](https://github.com/stutxo/simple_ctv),<br>[Optech](https://bitcoinops.org/en/topics/ephemeral-anchors/) | CTV + Pay To Anchor example | Prototype | ✓ | | | | |

## Tools

A collection of development and experimentation tools for CTV+CSFS.

| Name | Links | Description | Phase | CTV | CSFS | Use Case |
|------|-------|-------------|-------|-----|------|----------|
| CTV+CSFS Signet Node | [Repo](https://github.com/arshbot/ctv-csfs-signet-docker) | Docker-based Bitcoin node with CTV and CSFS enabled on MutinyNet signet | Production | ✓ | ✓ | Development, testing, prototyping, smart contract experimentation |
| CTV Playground | [Site](https://ctv.ursus.camp),<br> | Web-based tool for experimenting with CTV scripts and transaction templates | Prototype | ✓ | | Learning CTV concepts, testing script constructions, visualizing transaction templates |
| ctvlib | [Repo](https://github.com/ursuscamp/ctvlib),<br> | Rust utility library extracted from CTV Playground for CTV script development | Prototype | ✓ | | CTV script development, transaction template generation, library integration |
| Minsc | [Site](https://minsc-lang.org),<br>[v0.3](https://minsc-lang.org/v0.3),<br> | High-level scripting language for Bitcoin contracts with CTV support | Production | ✓ | | Policy development, script compilation, address generation, contract testing |
| Sapio Miniscript | [Docs](https://docs.rs/sapio-miniscript),<br>[Crate](https://crates.io/crates/sapio-miniscript),<br> | Production-ready Rust library for CTV+CSFS script development with Miniscript | Production | ✓ | ✓ | Production script development, protocol implementation, transaction analysis, PSBT integration |
| Sapio | [Repo](https://github.com/sapio-lang/sapio),<br> | Framework for creating composable multi-transaction Bitcoin Smart Contracts using CTV | Production | ✓ | | Smart contract development, CTV emulation, plugin integration |
| CTV Hash Generator | [Gist](https://gist.github.com/supertestnet/ad0ce4f92d1eecfc607b0b46afed7228) | JavaScript tool for generating CTV hashes using transaction data. | Prototype | ✓ | | CTV hash generation, transaction analysis. Passes all CTV test vectors.|

## Learning Resources

Educational materials about CTV+CSFS.

| Name | Author | Links | Description |
|------|--------|-------|-------------|
| OP_CSFS Wiki | Bitcoin Optech | [Topic](https://bitcoinops.org/en/topics/op_checksigfromstack/),<br> | Overview of OP_CHECKSIGFROMSTACK (OP_CSFS) opcode, its features, and potential applications in Bitcoin, including paying for signatures, delegation, oracles, and transaction introspection |
| Covenants 101 | Owen Kemeys | [Thread](https://x.com/OwenKemeys/status/1741575353716326835),<br> | Beginner-friendly explanation of CTV concepts, covering address construction, transaction templates, and practical applications |
| Templates, Eltoo, and Covenants | Jeremy Rubin | [Article](https://rubin.io/blog/2021/07/02/covenants/),<br> | Comprehensive analysis of CTV, CSFS, CAT, and APO upgrades, including safety considerations, design tradeoffs, and implementation recommendations |
| CSFS Re-Keying and Lightning Symmetry | Jeremy Rubin & Rearden | [Article](https://rubin.io/bitcoin/2024/12/02/csfs-ctv-rekey-symmetry/),<br> | Advanced technical exploration of CSFS re-keying techniques, key laddering, and applications to Lightning Network symmetry without extra signing round-trips |
| Credit Ecash + CTV | Ursus Camp | [Article](https://ursus.camp/bitcoin/2024/02/02/credit-ecash-and-check-template-verify.html),<br> | Exploration of combining CTV with non-custodial ecash for improved Lightning Network liquidity and privacy |
| Newbie Guide to OP_CTV | Katsu | [Article](https://bitcoindocs.org/notes/newbie-guide-to-check-template-verify-op-ctv),<br> | Learn the basics of CTV by building a locking address using CTV and executing a spend transaction that unlocks those funds |

## Community Discussions

Important technical discussions about OP_CTV and its applications.

| Topic | Date | Author | Links | Key Points |
|-------|------|--------|-------|------------|
| CSFS Implementation | Apr 10, 2025 | James O'Beirne | [PR](https://github.com/bitcoin/bitcoin/pull/32247),<br>[BIP](https://github.com/bitcoin/bips/blob/master/bip-0348.mediawiki),<br>[Docs](https://bitcoinops.org/en/topics/op_checksigfromstack/),<br> | Regtest-only deployment, Complements CTV, OP_SUCCESS behavior, Bundled deployment possible, Technical focus |
| CTV+CSFS as First Step | Mar 10, 2025 | Steven Roose | [Thread](https://delvingbitcoin.org/t/ctv-csfs-can-we-reach-consensus-on-a-first-step-towards-covenants/),<br> | Minimal package for covenants, Enables Lightning Symmetry, Simplifies DLCs and BitVM, Upgrade path to TXHASH, Focus on security and expressiveness |
| CTV Implementation | Mar 4, 2025 | James O'Beirne | [PR](https://github.com/bitcoin/bitcoin/pull/31989),<br>[BIP](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki),<br>[Docs](https://bitcoinops.org/en/topics/op_checktemplateverify/),<br> | Regtest-only deployment, Composable with CSFS/CAT, Well-tested implementation, No consensus changes, Focused on technical review |
| DLC Performance | Jan 24, 2022 | Lloyd Fournier | [Thread](https://gnusha.org/pi/bitcoindev/CAH5Bsr2vxL3FWXnJTszMQj83jTVdRvvuVpimEfY7JpFCyP1AZA@mail.gmail.com/),<br>[Paper](https://adiabat.github.io/dlc.pdf),<br>[BIP](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki),<br>[Spec](https://github.com/discreetlogcontracts/dlcspecs),<br> | 30x faster DLCs, No multiplications, Constant comms, Efficient oracles, Secure attestations |
| Eltoo Channel Comparison | Dec 29, 2021 | Jeremy Rubin & Michael Folkson | [Thread](https://bitcoin.stackexchange.com/questions/111497/how-do-eltoo-channel-constructions-using-anyprevout-compare-to-those-using-ctv-a),<br> | Fee payment challenges, CPFP vs RBF tradeoffs, Transaction size efficiency, Implementation complexity, Protocol equivalence |
| LN-Symmetry Implementation | Jan 6, 2020 | Jeremy Rubin | [BIP-119](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki#op_checksigfromstackverify),<br> | Floating transaction variant, Ephemeral anchors for fees, Self-reproducing automata, State transition restrictions, Fee payment alternatives |

*More discussions will be added as they are identified and analyzed.*

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. When adding new entries, please ensure they are relevant to CTV+CSFS specifically.

### Guidelines for Adding Projects
- Focus on projects that specifically use CTV+CSFS
- Include relevant links to documentation, code, and articles
- Clearly indicate the project phase (Implemented, Spec, Prototype, or Idea)
- List the primitives used in the implementation

## License

No license, no restriction
