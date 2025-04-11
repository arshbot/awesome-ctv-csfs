# Awesome CTV+CSFS

A curated list of resources, tools, and projects related to CHECKTEMPLATEVERIFY (CTV) and CAT+Simplicity (CSFS) in Bitcoin.

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
| Pool | • [Slides](https://notes.dunst.be/slide/#/2/slide/view/Ekky-cAegV9dSOaNOjH9TStNOmAnrhDDc9hxHlmRs5M/embed/present/)<br>• [Code](https://github.com/stutxo/op_ctv_payment_pool)<br>• [Sapio](https://github.com/sapio-lang/sapio/tree/master/plugin-example/payment_pool)<br>• [Article](https://rubin.io/bitcoin/2021/12/15/advent-18/)<br>• [Intro](https://rubin.io/bitcoin/2021/12/10/advent-13/)<br>• [IRC](https://freenode.irclog.whitequark.org/bitcoin-wizards/2019-05-21#24639752)<br>• [Coinpools](https://discrete-blog.github.io/coinpool/) | Scalable payment pool with CTV - supports up to 21 users, P2A fee management, and automatic coinjoin-like privacy | Prototype | ✓ | | | | |
| Vault | • [CTV Vault](https://github.com/jamesob/simple-ctv-vault)<br>• [Demo](https://github.com/jamesob/opvault-demo)<br>• [Sandwich](https://github.com/stutxo/Op_SecureTheSandwich) | Vault without pre-signed transactions | Prototype | ✓ | | | | |
| Android CTV Demo | • [Code](https://github.com/percy-g2/android_app_ctv_playground)<br>• [Release](https://github.com/percy-g2/android_app_ctv_playground/releases/tag/v0.1.0) | Native Android implementation demonstrating CTV Vault and payment pools with interactive UI | Prototype | ✓ | | | | |
| DLCs | • [Specs](https://github.com/discreetlogcontracts/dlcspecs/)<br>• [Cases](https://covenants.info/use-cases/dlcs/)<br>• [DLCAT](https://github.com/bennyhodl/dlcat) | 30x more performant DLCs | Prototype / Spec | ✓ | | ✓ | | ✓ |
| Transferable DLCs | - | Advanced DLC implementation | Idea | | | ✓ | ✓ | ✓ |
| Ark | • [Bark](https://codeberg.org/ark-bitcoin/bark/commits/branch/ctv) | Layer 2 protocol | Prototype | ✓ | | ✓ | | |
| BitVM | • [Thread](https://delvingbitcoin.org/t/how-ctv-csfs-improves-bitvm-bridges/1591) | Trust-minimized Bitcoin interoperability | Prototype | ✓ | ✓ | | ✓ | |
| Simple CTV | • [Code](https://github.com/stutxo/simple_ctv)<br>• [Optech](https://bitcoinops.org/en/topics/ephemeral-anchors/) | CTV + Pay To Anchor example | Prototype | ✓ | | | | |

## Tools

A collection of development and experimentation tools for CTV+CSFS.

| Name | Links | Description | Phase | CTV | CSFS | When to Use |
|------|-------|-------------|-------|-----|------|------------|
| CTV Playground | • [Site](https://ctv.ursus.camp/)<br>• [BIP](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki) | Web-based tool for experimenting with CTV scripts and transaction templates | Prototype | ✓ | | Learning CTV concepts through interactive examples |
| ctvlib | • [Repo](https://github.com/ursuscamp/ctvlib) | Rust utility library extracted from CTV Playground for CTV script development | Prototype | ✓ | | Adding CTV functionality to Rust applications |
| Minsc | • [Site](https://min.sc/)<br>• [v0.3](https://min.sc/v0.3/) | High-level scripting language for Bitcoin contracts with CTV support | Production | ✓ | | Writing complex CTV scripts in a high-level language |
| Sapio Miniscript | • [Docs](https://docs.rs/sapio-miniscript/latest/sapio_miniscript/)<br>• [Crate](https://crates.io/crates/sapio-miniscript) | Production-ready Rust library for CTV+CSFS script development with Miniscript | Production | ✓ | ✓ | Building production applications with CTV+CSFS and Miniscript |

## Learning Resources

Educational materials about CTV+CSFS.

| Name | Author | Links | Description |
|------|--------|-------|-------------|
| Covenants 101 | Owen Kemeys | • [Thread](https://x.com/OwenKemeys/status/1741575353716326835) | Beginner-friendly explanation of CTV concepts, covering address construction, transaction templates, and practical applications |
| Templates, Eltoo, and Covenants | Jeremy Rubin | • [Article](https://rubin.io/blog/2021/07/02/covenants/) | Comprehensive analysis of CTV, CSFS, CAT, and APO upgrades, including safety considerations, design tradeoffs, and implementation recommendations |
| CSFS Re-Keying and Lightning Symmetry | Jeremy Rubin & Rearden | • [Article](https://rubin.io/bitcoin/2024/12/02/csfs-ctv-rekey-symmetry/) | Advanced technical exploration of CSFS re-keying techniques, key laddering, and applications to Lightning Network symmetry without extra signing round-trips |

## Community Discussions

Important technical discussions about OP_CTV and its applications.

| Topic | Date | Author | Links | Key Points |
|-------|------|--------|-------|------------|
| DLC Performance | Jan 24, 2022 | Lloyd Fournier | • [Thread](https://gnusha.org/pi/bitcoindev/CAH5Bsr2vxL3FWXnJTszMQj83jTVdRvvuVpimEfY7JpFCyP1AZA@mail.gmail.com/)<br>• [Paper](https://adiabat.github.io/dlc.pdf)<br>• [BIP](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki)<br>• [Spec](https://github.com/discreetlogcontracts/dlcspecs) | • 30x faster DLCs<br>• No multiplications<br>• Constant comms<br>• Efficient oracles<br>• Secure attestations |
| CTV Implementation | Mar 4, 2025 | James O'Beirne | • [PR](https://github.com/bitcoin/bitcoin/pull/31989)<br>• [BIP](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki)<br>• [Docs](https://bitcoinops.org/en/topics/op_checktemplateverify/) | • Regtest-only deployment<br>• Composable with CSFS/CAT<br>• Well-tested implementation<br>• No consensus changes<br>• Focused on technical review |
| CSFS Implementation | Apr 10, 2025 | James O'Beirne | • [PR](https://github.com/bitcoin/bitcoin/pull/32247)<br>• [BIP](https://github.com/bitcoin/bips/blob/master/bip-0348.mediawiki)<br>• [Docs](https://bitcoinops.org/en/topics/op_checksigfromstack/) | • Regtest-only deployment<br>• Complements CTV<br>• OP_SUCCESS behavior<br>• Bundled deployment possible<br>• Technical focus |
| CTV+CSFS as First Step | Mar 10, 2025 | Steven Roose | • [Thread](https://delvingbitcoin.org/t/ctv-csfs-can-we-reach-consensus-on-a-first-step-towards-covenants/1509) | • Minimal package for covenants<br>• Enables Lightning Symmetry<br>• Simplifies DLCs and BitVM<br>• Upgrade path to TXHASH<br>• Focus on security and expressiveness |
| Eltoo Channel Comparison | Dec 29, 2021 | Jeremy Rubin & Michael Folkson | • [Thread](https://bitcoin.stackexchange.com/questions/111497/how-do-eltoo-channel-constructions-using-anyprevout-compare-to-those-using-ctv-a) | • Fee payment challenges<br>• CPFP vs RBF tradeoffs<br>• Transaction size efficiency<br>• Implementation complexity<br>• Protocol equivalence |
| LN-Symmetry Implementation | Jan 6, 2020 | Jeremy Rubin | • [BIP-119](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki#op_checksigfromstackverify) | • Floating transaction variant<br>• Ephemeral anchors for fees<br>• Self-reproducing automata<br>• State transition restrictions<br>• Fee payment alternatives |

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