"HEW Crypto Market" Requirements Definition Document

Created: July 10, 2026　　Last updated: ___, ___, ___

- Class: IH12A233　　Group number: IH12A-04
- Team size: 5 members (team project)
- Members: Anthony / Battulga / Nakayama / To /
- Target exhibition: HEW (department exhibition; scheduled for approximately March 2027; exact date TBD)

### 1. Revision history

| Version | Date | Changes | Author |
|---|---|---|---|
| 1.0 | TBD | Initial draft | |

---

## 2. Project overview

### 2.1 Theme

HEW Crypto Market — A Simulated Crypto Investment Experience

### 2.2 Overview

An exhibition-based simulated investment experience in which visitors use 1,000 HEWCoin to trade three types of tokens and experience market price fluctuations.

### 2.3 Background

Interest in investing and cryptocurrency is growing, but there are few opportunities to experience investing firsthand. Exhibits that handle real financial assets or money carry significant legal and safety risks, making them unsuitable for a school exhibition. We therefore propose a simulated market called "HEWCoin" that is entirely self-contained within the venue, allowing visitors to safely experience how the value of their assets can increase or decrease through trading.

### 2.4 Purpose

The purpose of this project is to allow visitors to experience, within a short period of time, how the value of their assets can increase or decrease through simulated trading.

### 2.5 Supported platform

Web browser (accessible only through the on-campus network and not publicly available outside the school)

---

## 3. Glossary

| Term | Description |
|---|---|
| HEWCoin | A simulated currency used only within the exhibition. Each visitor initially receives 1,000 HEWCoin. HEWCoin cannot be exchanged for real money. |
| Token | A simulated asset traded by visitors. Three token types are available: GAME, CG, and WEB. |
| Liquidity | A value assigned to each token. The higher the liquidity, the smaller the price change caused by a trade of the same amount. |
| Volatility coefficient | A coefficient used to adjust the degree of a token's price movement. |
| Fluctuation rate | The percentage by which a token's price changes after a single trade. It is calculated based on the trade amount, liquidity, and volatility coefficient. |
| Total assets | The sum of a visitor's HEWCoin balance and the current value of all tokens held, calculated as the quantity held multiplied by the current token price. |

---

## 4. Target users

| User type | Description |
|---|---|
| Visitor | A general visitor who registers a nickname and accesses the trading screen from a smartphone to experience simulated investing. |
| Operations staff (development team) | Exhibition staff responsible for operating the system, handling technical issues, closing the market on the final day, and announcing the final rankings. |

---

## 5. Functional requirements

### 5-1. Version 1.0 in-scope features

| # | Feature | Description (what it does) | Priority |
|---|---|---|---|
| 1 | Initial HEWCoin allocation | Allocate 1,000 HEWCoin to each newly registered visitor. | High |
| 2 | Token trading | Visitors can choose from GAME, CG, or WEB and buy or sell tokens in transaction amounts of 100, 300, or 500 HEWCoin. The token price updates after every completed transaction. | High |
| 3 | Asset overview | View the visitor's HEWCoin balance, token holdings, and total asset value. | Medium |
| 4 | Ranking display | Display a real-time ranking of visitors based on their total asset values. | Medium |
| 5 | Additional HEWCoin allocation | Provide additional HEWCoin to visitors whose balances are too low to continue trading. No real-money transactions are involved. | Low |
| 6 | My page | View the visitor's nickname, token holdings, account balance, and trade history. | High |
| 7 | Registration screen | Visitors register a nickname to create a temporary exhibition account. Their assets and trade history can be retained across multiple days of attendance. | High |
| 8 | Market list | View the current price and recent price movement of each token. | Medium |
| 9 | Final ranking announcement | Close the market on the final day, calculate the final total asset values, finalize the rankings, and announce the results. | High |

### 5-2. Version 1.0 out-of-scope features

| # | Feature | Reason for exclusion |
|---|---|---|
| 1 | Chat | A communication feature between visitors is excluded from Version 1.0 so the team can focus on the trading experience. |
| 2 | News | A news feed explaining or dramatizing the causes of price movements could improve the experience, but it is excluded from Version 1.0 because of its implementation cost. |
| 3 | Market reset | The market will operate continuously throughout the two- to three-day exhibition period and will close on the final day. Therefore, a market reset feature is not required. |
| 4 | Identity verification and account authentication | Only nickname-based registration will be implemented. Email authentication, identity verification, and full account management will not be included. |

---

## 6. Non-functional requirements

| # | Category | Content |
|---|---|---|
| 1 | Access scope | The system is published only within the on-campus network and is not made publicly available outside the school. |
| 2 | Security | The system must collect only the minimum amount of user information required. Access must be restricted to the on-campus network. |
| 3 | Response speed | The system must reflect user actions on the screen within a few seconds, even when multiple visitors access the system concurrently. |
| 4 | Availability | The system must operate continuously and reliably throughout the exhibition period. An error caused by one visitor's actions must not affect other visitors. |
| 5 | Usability | The user interface must be intuitive and easy to understand, even for visitors with no prior knowledge of cryptocurrency or investing. |

---

## 7. Constraints and assumptions

- The event runs for 2–3 days. The market is not reset during this period; it is stopped on the final day, and the final ranking is announced.
- The system is published only within the on-campus network and is not made publicly available outside the school.
- Visitors will register a nickname and access the service using their own smartphones.
- Development and operation are handled by a team of 5 members.

---

## 8. Team and schedule

### 8-1. Role assignment

| Assignee | Role |
|---|---|
| Nakayama | Project lead / documentation (progress management; finalizing the requirements and design documents) |
| Anthony | Frontend development and UI/UX design (screen implementation; colors, icons, and other visual design) |
| To | Backend development (API implementation, price-fluctuation logic, database design and implementation) |
| Battulga | Infrastructure, testing, and exhibition operations (on-campus server/network setup, QA, on-site operation during the exhibition) |
| [Member 5] | [Role TBD] |

### 8-2. Schedule

| Phase | Content | Target period |
|---|---|---|
| Requirements definition / basic design | Finalize the requirements definition and design documents. | Week 1 |
| Basic implementation | Build the database, API, and initial user interface structure. | TBD |
| Feature implementation | Implement trading logic, ranking, and registration features. | TBD |
| UI refinement / integration testing | Refine the UI and conduct end-to-end testing. | TBD |
| Rehearsal / final adjustments | Test under conditions similar to the actual exhibition environment and fix bugs. | TBD |
| Exhibition-day operation | Operate the system during the HEW event (around March 2027); close the market and announce the ranking on the final day. | TBD |

The detailed schedule will be determined by working backward from the official HEW exhibition date once it is confirmed.

---

## 9. Risks and issues

| # | Risk / issue | Response |
|---|---|---|
| 1 | The on-campus Wi-Fi may have limitations on the number of concurrent connections and available bandwidth. | Minimize network traffic and conduct concurrent-user and load testing in advance. |
| 2 | The development period is short, which limits the amount of functionality that a five-person team can implement. | Narrow the Version 1.0 scope (see Section 5) and defer lower-priority features. |
| 3 | Visitor congestion on exhibition days could cause operational bottlenecks. | Estimate visitor flow, prepare clear operating procedures, and conduct load testing based on the expected number of concurrent users. |
| 4 | Uneven skill distribution among members could cause differences in progress across areas. | Hold regular progress meetings, share technical knowledge, and reassign tasks when necessary. |

---

## 10. Related documents

- One-sheet proposal (HEW_企画書_IH12A-04.pptx)
- HEW Crypto Market design document (HEW_Crypto_Market_設計書.md)
- HEW Crypto Market requirements definition document (this document)
