# 📈 Silicon Chain: Dynamic iPhone Price Forecasting Engine

An interactive supply chain simulator designed to model how real-time semiconductor macro-anomalies, lithography bottlenecks, wafer fabrication outputs, and logistics disruptions dictate downstream consumer retail pricing across Apple's device portfolio over a 6-month horizon.

---

## 🚀 How to Run This Program (Zero-Dependency Local Launch)

This application is built using a lightweight, highly efficient **Single-File Architecture** designed to execute entirely client-side. It runs natively inside any modern web browser without requiring heavy background runtimes, local server instances, or package dependencies (e.g., Node.js or Docker). This ensures peak execution even on vintage or hardware-constrained environments (like a 2017 MacBook).

### Step-by-Step Execution:
1. Clone this repository to your local directory:
   ```bash
   git clone https://github.com
   ```
2. Navigate into the cloned folder:
   ```bash
   cd silicon-chain-predictor
   ```
3. Locate the `index.html` file and open it directly with your choice of web browser:
   * **Via Finder/GUI:** Double-click the `index.html` file to launch it in your default web browser (Safari, Chrome, or Firefox).
   * **Via Terminal (Mac OS):** Execute the following command:
     ```bash
     open index.html
     ```
4. Adjust the **Supply Parameter Sliders** on the left panel to inject global supply chain shocks and view the compounding 6-month retail price adjustments dynamically calculated in real-time.

---

## 🧠 Structural Bill-of-Materials (BOM) Component Matrix & Parameter Weights

Rather than utilizing flat, arbitrary pricing multipliers, this forecasting engine relies on a product-specific structural matrix. Each iPhone model draws an isolated percentage of its baseline production value from distinct supply chain nodes. When a global supply shock hits, it compounds uniquely based on a model's true hardware bill-of-materials (BOM) asset weight allocation.

### Detailed Model Parameter Breakdown:

```javascript
const modelComponentMatrix = {
    duo:   { premiumNodes: 0.40, packaging: 0.25, specialtyHinges: 0.25, baseLogistics: 0.10 }, 
    proMax:{ premiumNodes: 0.45, packaging: 0.35, specialtyHinges: 0.00, baseLogistics: 0.20 }, 
    pro:   { premiumNodes: 0.45, packaging: 0.30, specialtyHinges: 0.00, baseLogistics: 0.25 }, 
    air:   { premiumNodes: 0.30, packaging: 0.20, specialtyHinges: 0.00, baseLogistics: 0.50 }, 
    i17:   { premiumNodes: 0.20, packaging: 0.10, specialtyHinges: 0.00, baseLogistics: 0.70 }, 
    i17e:  { premiumNodes: 0.10, packaging: 0.05, specialtyHinges: 0.00, baseLogistics: 0.85 }  
};
```

### Technical & Strategic Weight Rationale:

#### 1. 📱 iPhone Duo (Foldable Flagship)
* **Weights:** `premiumNodes: 40%`, `packaging: 25%`, `specialtyHinges: 25%`, `baseLogistics: 10%`
* **Rationale:** As a cutting-edge foldable form factor, its pricing is heavily volatile. It demands premium bleeding-edge computing nodes (40%) and high packaging tolerances. Crucially, it dedicates **25% of its systemic parameter weight to custom mechanical hinge manufacturing**. Foldable hinges encounter low yield thresholds and specialized mechanical component bottlenecks, compounding retail price fluctuations when lithography capacity suffers.

#### 2. 🚀 iPhone 18 Pro & Pro Max (Bleeding-Edge Silicons)
* **Weights (Pro Max):** `premiumNodes: 45%`, `packaging: 35%`, `specialtyHinges: 0.00`, `baseLogistics: 20%`
* **Rationale:** The Pro and Pro Max architectures demand the absolute maximum reliance on bleeding-edge TSMC wafer fabrication processing (45%). More importantly, they allocate **35% weight to advanced CoWoS packaging pipelines**. Because advanced AI accelerator processing chips heavily oversubscribe CoWoS packaging facilities globally, any yield shock in advanced packaging triggers immediate downstream margin pressure, forcing aggressive retail price pass-throughs.

#### 3. 💨 iPhone Air (Ultra-Thin Architecture)
* **Weights:** `premiumNodes: 30%`, `packaging: 20%`, `specialtyHinges: 0.00`, `baseLogistics: 50%`
* **Rationale:** The Air focuses on structural optimization rather than high-performance computing clusters. While it uses mature advanced processing nodes, **50% of its weight is tied directly to logistics, transport, and structural form factor assembly overhead**. 

#### 4. 🍂 iPhone 17 & 17e (Legacy / Commodity Scale)
* **Weights (17e):** `premiumNodes: 10%`, `packaging: 5%`, `specialtyHinges: 0.00`, `baseLogistics: 85%`
* **Rationale:** The baseline iPhone 17 and budget-friendly 17e utilize highly mature, scaled, older-generation nodes. Because their silicon yields are practically maxed out and advanced, scarce packaging is not required, their manufacturing costs are insulated from fabrication squeezes. Instead, **85% of their production parameters rely on base global assembly logistics, transport, and raw commodity shipping elements**, making them stable product offerings unless transport lanes freeze.
