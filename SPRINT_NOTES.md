# Kuira Sprint Notes

## What I built

I built a minimal proof counter for the Kuira/Midnight sprint. The contract stores a public `round` counter and exposes an `increment()` circuit.

## Why this project

I wanted a very small contract so the interesting part of the sprint is the mobile proving experience rather than application complexity.

## Contract walkthrough

`round` is a `Counter` ledger field. It starts at zero.

`increment()` is the exported circuit. Each successful call increases `round` by one.

## Phone proving

Fill this section only after testing on a real Android device.

- Device:
- Android version:
- Kuira SDK version:
- Approximate proving time:
- Was proving completed without a proof server?:
- Screenshot/video evidence:

## What I would build next

The next version could turn this into a private voting demo with a passkey-based identity and a richer privacy-preserving contract flow.
