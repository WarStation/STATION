# 🛰️ WARSTATION: OPERATIONAL COMMAND NODE

**Warstation** is a mission-critical operational node designed for digital tacticians, builders, and operators. It consolidates fragmented workflows into a single, high-precision interface for token deployment, geopolitical visualization, and system diagnostics.

---

## ⚡ MISSION OVERVIEW

In an era of digital noise, Warstation provides focus. It is not just an application; it is an intentional workspace built for speed, precision, and tactical execution.

- **Status**: `OPERATIONAL`
- **Node ID**: `0x7F2A`
- **Protocol**: `SECURE_TUNNEL_v4.1`
- **X (Twitter)**: [WarStationSol](https://x.com/WarStationSol)
- **GitHub**: [WarStation/STATION](https://github.com/WarStation/STATION)

---

## 🛠️ CORE MODULES

### 1. DEPLOY TOKEN & POOL (`/deploy`)
The **Deploy Station** is the primary engine for asset initialization. It allows operators to launch tokens and establish liquidity pools with granular control.

- **Token Initialization**: Define name, symbol, and supply with zero-latency execution.
- **Pool Configuration**: Set initial liquidity, fee tiers, and pair parameters.
- **Real-time Validation**: Integrated diagnostic checks for contract integrity before deployment.

### 2. WAR ROOM (`/war-room`)
A high-tech visualization theater built with **D3.js** and **TopoJSON**.

- **Global Theater**: 3D interactive globe highlighting active operational zones (e.g., US vs. Iran theater).
- **Trajectory Simulation**: Real-time missile trajectory animations with impact diagnostics.
- **Signal Feed**: Live satellite uplink simulation and target acquisition telemetry.
- **DEFCON Status**: Dynamic threat level monitoring and alert system.

### 3. COMMAND NODE (`/command-node`)
The system's initialization sequence and diagnostic dashboard.

- **Kernel Boot**: Real-time logging of system initialization and encrypted uplink establishment.
- **Diagnostics**: Live monitoring of CPU load, memory allocation, and firewall integrity.
- **Operational Logs**: Persistent tracking of node activity and operator sessions.

---

## 🚀 INSTALLATION

### Prerequisites
- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher

### 1. Clone the Repository
```bash
git clone https://github.com/your-org/warstation.git
cd warstation
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment
Create a `.env` file in the root directory:
```env
GEMINI_API_KEY=your_api_key_here
VITE_NETWORK_ID=mainnet
VITE_OPERATOR_ID=0x...
```

### 4. Launch Command Node
```bash
npm run dev
```
The station will be accessible at `http://localhost:3000`.

---

## 🔌 INTEGRATION GUIDE

### Connecting to the Fleet
To integrate Warstation with your existing infrastructure, use the following patterns:

#### Token Deployment Hook
```typescript
import { deployToken } from './services/deployService';

const mission = await deployToken({
  name: "TACTICAL_ASSET",
  symbol: "TAC",
  supply: 1000000
});

console.log(`Mission Initialized: ${mission.txHash}`);
```

#### War Room Signal Feed
The War Room accepts external signal feeds via the `SignalService`. Ensure your data follows the `GeoJSON` standard for optimal projection.

---

## 📖 API REFERENCE

### `GET /api/status`
Returns the current operational status of the node.
- **Response**: `200 OK`
- **Payload**: `{ status: "OPERATIONAL", uptime: "142h", load: 0.42 }`

### `POST /api/deploy/token`
Initializes a new token deployment sequence.
- **Body**: `{ name: string, symbol: string, supply: number }`
- **Response**: `201 Created`

### `GET /api/war-room/telemetry`
Fetches the latest target acquisition data for the globe visualization.
- **Response**: `200 OK`

---

## 🧬 TECH STACK

- **Frontend**: React 19, Vite, Tailwind CSS 4.0
- **Animation**: Motion (Framer Motion), D3.js
- **Icons**: Lucide React
- **Routing**: React Router 7
- **AI Engine**: Google Gemini API (@google/genai)
- **Data**: TopoJSON, Better-SQLite3

---

## 📄 LICENSE

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

> **WARNING**: Unauthorized access to the Warstation command node is strictly prohibited. All sessions are logged and monitored by the system kernel.
