# Awesome CTV+CSFS

A curated list of resources, tools, and projects related to CHECKTEMPLATEVERIFY (CTV) and CAT+Simplicity (CSFS) in Bitcoin.

## Table of Contents
- [Projects](#projects)
- [Tools](#tools)
- [Learning Resources](#learning-resources)
- [Contributing](#contributing)

## Projects

A collection of interesting projects utilizing covenants, particularly focusing on CTV+CSFS implementations.

| Name | Links | Description | Phase | Primitives |
|------|-------|-------------|-------|------------|
| Pool | [Slides](https://notes.dunst.be/slide/#/2/slide/view/Ekky-cAegV9dSOaNOjH9TStNOmAnrhDDc9hxHlmRs5M/embed/present/)<br>[Implementation](https://github.com/stutxo/op_ctv_payment_pool)<br>[Sapio Example](https://github.com/sapio-lang/sapio/tree/master/plugin-example/payment_pool)<br>[Article](https://rubin.io/bitcoin/2021/12/15/advent-18/) | Rolling coinjoin (joinpool) | Prototype | CHECKTEMPLATEVERIFY |
| Payment Pool | - | Payment pool implementation | Prototype | CHECKTEMPLATEVERIFY |
| Vault | [Simple CTV Vault](https://github.com/jamesob/simple-ctv-vault)<br>[OPVault Demo](https://github.com/jamesob/opvault-demo)<br>[SecureTheSandwich](https://github.com/stutxo/Op_SecureTheSandwich) | Vault without pre-signed transactions | Prototype | CHECKTEMPLATEVERIFY |
| Dynamic Vaults | - | Advanced vault implementation | Prototype | VAULT / CHECKCONTRACTVERIFY |
| DLCs | [DLC Specs](https://github.com/discreetlogcontracts/dlcspecs/)<br>[Use Cases](https://covenants.info/use-cases/dlcs/)<br>[DLCAT](https://github.com/bennyhodl/dlcat) | 30x more performant DLCs | Prototype / Spec | CHECKTEMPLATEVERIFY / TXHASH / CHECKCONTRACTVERIFY |
| Transferable DLCs | - | Advanced DLC implementation | Idea | CAT / TXHASH / CHECKCONTRACTVERIFY |
| Ark | [Bark Implementation](https://codeberg.org/ark-bitcoin/bark/commits/branch/ctv) | Layer 2 protocol | Prototype | CHECKTEMPLATEVERIFY / TXHASH |

## Tools

*Coming soon - Tools and libraries for working with CTV+CSFS*

## Learning Resources

*Coming soon - Educational materials about CTV+CSFS*

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. When adding new entries, please ensure they are relevant to CTV+CSFS specifically.

### Guidelines for Adding Projects
- Focus on projects that specifically use CTV+CSFS
- Include relevant links to documentation, code, and articles
- Clearly indicate the project phase (Implemented, Spec, Prototype, or Idea)
- List the primitives used in the implementation

## License

This project is licensed under the MIT License - see the LICENSE file for details.
