# The Manifesto

**1. The Status Quo is the Bottleneck**
Financial accounting is the backbone of every company. Yet, the existing software landscape stems from an era when accounting meant "manual labor." GUI-first approaches, manual confirmations, and rigid database schemas are today’s biggest stumbling blocks on the path to true efficiency. In a world where transactions happen in milliseconds, accounting must not think in days.

**2. Headless & Radically Extensible**
We are not building rigid tables, but a flexible data foundation. Every object—whether a transaction, an account, or a ledger—can be enriched with arbitrary metadata. We do not dictate *what* is stored, but provide the structure to ensure *that* it is handled in a type-safe and performant manner. Whether invoice IDs, cost centers, or vector embeddings—the context lives within the record. This flexibility makes the core the ideal basis for specialized business environments without bloating the core itself.

**3. Finance as Code**
Financial policy belongs in the code, not in PDF manuals. Compliance rules, expense limits, and depreciation logic are defined directly within the core as executable and researchable logic. The system acts as a gatekeeper: It either verifies retroactively or validates transactions in real-time against these stored rules. Anything that does not comply with the rules is rejected by the core—technically guaranteed.

**4. Agnostic Accounting**
The core itself knows no HGB, IFRS, or US-GAAP. It is a neutral mathematical machine. Accounting standards are merely **interchangeable configuration layers**.
*   **Composable Compliance:** You define, for example, "IFRS". The engine applies these rules to the transactions to generate a specific view.
*   **Concurrency:** You can apply any number of sets simultaneously to the same data foundation without duplicating the data.

**5. Native Multi-Currency & Commodity Agnosticism**
To the engine, money is just one of many resources. We treat currencies (EUR, USD) and crypto assets (BTC) equally.
*   **No Base Currency:** There is no forced "base currency" in storage. Transactions are preserved in their original unit.
*   **Realtime FX:** Currency conversions and exchange rate gains/losses are pure projections at the time of the query, based on defined rules.

**6. The Continuous Close**
We are eliminating the "month-end close" as an event. Through event sourcing and dynamic views, the books are *always* closed. A balance sheet is not a static report, but a status retrievable at any time. We do not wait for batch jobs; financial reality is transparent at every moment, down to the exact millisecond.

**7. Performance & Integrity via Rust**
To enable complex simulations and real-time reporting on demand, the operative core lives efficiently in memory, secured by immutable append-only logs. We provide the robust infrastructure upon which others can build with maximum data security.

**8. Extensibility**
We strictly separate the **Core** from the **Extensions**.
*   **The Core:** Manages facts, multi-currency logic, and rule sets. It is incorruptible and exact.
*   **The Extensions:** Reconciliation, OCR, or AI analyses are separate satellites. They provide input, but the core decides.