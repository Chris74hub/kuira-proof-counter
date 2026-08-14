# Kuira Proof Counter

A small Midnight Compact contract prepared for the Kuira Android SDK sprint.

The project demonstrates the basic contract flow:

1. A Compact contract keeps a counter on the Midnight ledger.
2. The `increment()` circuit changes the ledger state.
3. The Kuira Android SDK can run the contract runtime and ZK proving on the Android device.
4. The app can deploy the contract and call `increment()` from the phone.

## Contract

`contract/src/proof_counter.compact` contains the core contract:

- `round` starts at zero.
- `increment()` increases it by one.
- The contract is intentionally small so the proving/deployment flow is easy to understand.

## Kuira

Kuira is an Android SDK for Midnight with on-device ZK proving, passkey identity, an embedded wallet and the Compact runtime.

Official SDK documentation:
https://kuiralabs.github.io/kuira-sdk-android/

The current Kuira documentation shows the `dapp-ui` dependency as:

```kotlin
implementation("io.github.kuiralabs:dapp-ui:0.1.0-alpha05")
```

Use the Kuira Starter as the Android app shell, then replace its demo contract with the contract in this repository. The exact starter integration should be kept aligned with the current Kuira recipe because the SDK is still in alpha.

## Build story

For the sprint write-up, document:

- what the contract does;
- how you connected it to the Kuira Android app;
- deployment and contract-call steps;
- what it felt like generating the proof on your phone;
- what you would build next.

Do not claim a proof was generated on-device until you have actually run the app on an Android device and captured evidence.

## Suggested next step

Clone the official Kuira Starter, get it running first, then copy:

`contract/src/proof_counter.compact`

into the starter's contract source directory and follow the Kuira `Deploy and call a Compact contract` recipe.

This repository is the sprint-specific contract/documentation layer; the generated build artifacts and secrets should not be committed.
