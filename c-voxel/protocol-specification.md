---
description: Here is C-Voxel's Spec.
---

# 📖 Protocol Specification

## Visualization

For alpha C-Voxel, "Genre" and "DAO" properties are not implemented yet.

![visualization schema](../.gitbook/assets/cvoxel\_logic.png)

## Data Model

Each C-Voxel contains the work detail data and related transaction hash.

Here is C-Voxel's Data Model&#x20;

```
  to: string; // payee address. maybe contract address
  from: string; // payer address. maybe contract address
  isPayer: boolean; // whether owner is payer or not
  summary: string; // work summary
  detail: string; // work detail. Optional.
  deliverable: string; // deliberable link. Optional.
  value: string; // reward value
  tokenSymbol: string; // eth, usdc, etc
  tokenDecimal: number;
  fiatValue: string; //reward value as USD. Optional.
  fiatSymbol: string; // currently only USD supported. Optional.
  networkId: number; // eth mainnet = 1 | polygon mainnet = 137
  issuedTimestamp: string; //block timestamp
  txHash: string; // transfer tx hash
  relatedTxHashes: string[]; //txes releated the work. Optional.
  tags: string[]; //tags
  genre: string; // main genre. Optional.
  jobType: "FullTime" | "PartTime" | "OneTime"; // default=OneTime
  toSig: string; // sig of payee
  fromSig: string; // sig of payer
  toSigner: string; // who signed this cvoxel as payee actually. Only EOA supported
  fromSigner: string; // who signed this cvoxel as payer actually. Only EOA supported
  relatedAddresses: string[]; // all addresses related to this cvoxel. may contain both EOA and contract address
```
