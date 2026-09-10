# DF26 - Pronto customizations for the "Intro to Agentforce Vibes" demo

## About

This branch (`df26-afv-demo`) is the **lean demo project** used in the DF26 AI Force Theater
_"Intro to Agentforce Vibes"_ session. It runs against a **pre-provisioned Pronto org** and is
meant to be opened in the **Agentforce Vibes** browser IDE.

It ships:

- `sample-prompts.md` — the six demo prompts (count storefronts → build `latestOrderCard` LWC →
  Apex tests → Code Analyzer → open-record button → build `openingHoursCard` from an image).
- `sample-opening-hours.jpg` — the hand-drawn image used by the multimodal prompt (Prompt 6).
- `.afv/rules/pronto-rules.md` — Agentforce Vibes rules for the Pronto project.
- `reset-demo.sh` + `reset-metadata/` — resets the org between presenters.

## Prerequisites

- A **Pronto org** already provisioned with the base app + data (storefronts, orders, the
  **Merchant Management** app, the **Storefront Explorer** page, the **Storefront** record page,
  and the existing `StoreController.getHoursOfOperation` method used by Prompt 6). If you need to
  build the base org from scratch, use the `main` branch's setup (`./bin/install.sh` + data plan).
- The Vibes IDE terminal authenticated to that org as the **default target org** (`sf org display`).

## First-time setup (in the Agentforce Vibes IDE terminal)

```sh
sf update
npm install
```

## Reset the demo (before every talk)

```sh
./reset-demo.sh
```

Then close all IDE tabs and clear the Dev Agent history.
