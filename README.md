# A SOLID implementation in Rust

## Architecture
The architecture is based on the description [here](https://rubenverborgh.github.io/solid-server-architecture/solid-architecture-v1-3-0.pdf). 
Authentication and authorization are cobined to one crate `auth`.

- Auth
- CLI
- Core
- LDP
- Server
- Storage

## An Encrypted Data Vault

> Solid is a Secure Storage Provider for Linked Data

We store a significant amount of sensitive data online, such as personally identifying information (PII), trade secrets, family pictures, and customer information. The data that we store is often not protected in an appropriate manner.


### Differences between Solid and IPFS

**Solid**
- File and graph store
- Spec requires no encyption
- Extended file metadata is supported
- Read/write protocol: REST (LDP)
- Auth: WebID-OIDC	
- Data locality: Server
- Replication: None
- Access Control: [Web Access Control (WAC)] (https://github.com/solid/web-access-control-spec)

**IPFS**
- Content-addressable distributed file store
- Spec requires no encyption
- Extended file metadata is not supported
- Read/write protocol: cli/HTTP
- Data locality: Public nodes
- Replication: [Peer to peer](https://discuss.ipfs.io/t/replication-on-ipfs-or-the-backing-up-content-model/372)
- Access Control: [None](https://github.com/ipfs/notes/issues/376)