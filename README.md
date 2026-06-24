# CryptoBallot

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-yellow)
![License](https://img.shields.io/badge/license-View--Only-lightgrey)
![Status](https://img.shields.io/badge/status-active-brightgreen)

A simulated biometric multi-factor authentication voting system — a front-end demonstration of secure, transparent digital elections.

## Stack

- HTML5 / CSS3 / Vanilla JavaScript (ES6+)
- No frameworks — pure static front-end
- JSON-based voter database

## How it works

CryptoBallot walks a voter through a 5-step authentication and voting wizard:

```mermaid
flowchart TD
    A[index.html] --> B[Start Voting]
    B --> C[Step 1: Iris Scan]
    C --> D{Valid Iris ID?}
    D -->|No| C
    D -->|Yes| E[Step 2: NFC Activation]
    E --> F{Valid NFC tag?}
    F -->|No| E
    F -->|Yes| G[Step 3: Face Recognition]
    G --> H[Display voter photo + name]
    H --> I[Confirm identity]
    I --> J[Step 4: Voting Booth]
    J --> K[Select party A-E]
    K --> L[Step 5: Confirmation]
    L --> M[Vote recorded]
    M --> N[Auto-reset after 3s]
    N --> B
```

1. **Iris Scan** — voter enters a pre-registered Iris ID
2. **NFC Activation** — voter enters an NFC tag ID
3. **Face Recognition** — matched voter photo and name are displayed for confirmation
4. **Voting Booth** — voter selects one of five parties
5. **Confirmation** — vote recorded message with session reset

All voter data is loaded from a static `voters.json` file. The entire flow runs client-side with no backend dependency.

## Key features

- 3-factor authentication simulation (biometric, possession, confirmation)
- 5-step wizard with step-by-step navigation
- Dark cyber aesthetic with cyan/teal accent palette
- Double-vote prevention within a session
- Console-logged "blockchain" vote recording simulation

## What this demonstrates

- Building a complete multi-step UI wizard from scratch
- State management in vanilla JavaScript
- Dark-themed UI design with CSS custom properties
- Form validation and user flow design

## Run locally

Open `new/index.html` in any browser. No server required.
