# IRIN-Risk-Auditor
Document a Violation Take a photo. Get legal guidance. Protect yourself.  No file chosen 📷 Tap to take photo or video  Auto-timestamped &amp; hashed
# IRIN Core

**Infrastructure Risk Intelligence Network**

> A global, tamper-evident map for reporting and tracking infrastructure risks.
> 
> **Client-side only. No server. No blockchain. Free forever.**

---

## What Is IRIN?

IRIN lets anyone:

1. **Upload evidence** of infrastructure problems (photos, videos, documents)
2. **Pin the location** on a global map
3. **Create a cryptographic proof** that the evidence hasn't been altered
4. **Build a chain** of linked entries that can't be tampered with undetected

All data stays in your browser. Nothing is uploaded to any server.

---

## How It Works

### 1. Upload → Hash
When you upload a file, IRIN computes its **SHA-256 hash** — a unique fingerprint. If even one pixel changes, the hash changes completely. This proves your file hasn't been altered.

### 2. Map → Locate
Click anywhere on the globe to set the location of the incident. Use 3D mode for cinematic view, 2D mode for faster performance.

### 3. Submit → Chain
Your entry is saved locally and linked to the previous entry. Break the chain, and it's immediately detected during verification.

### 4. Verify → Trust
Anyone can verify the entire ledger with one click. If any entry has been tampered with, the chain breaks and turns red.

---

## Key Features

| Feature | Description |
|---------|-------------|
| **3D/2D Globe** | CesiumJS 3D + Leaflet 2D with auto device detection |
| **Active Tracking** | Pulsing markers show live risk hotspots |
| **Risk Heatmap** | Visual intensity based on severity |
| **Client Hashing** | SHA-256 computed in your browser |
| **Tamper Detection** | Chain-linked entries break if altered |
| **Monthly Anchors** | Generate cumulative hashes for public proof |
| **Evidence Export** | Download full ledger as JSON |

---

## Is This Blockchain?

**No.**

IRIN Core is **client-side only**:
- No blockchain
- No cryptocurrency
- No gas fees
- No wallet needed
- No server
- No database

Everything runs in your browser using:
- **IndexedDB** for local storage
- **Web Crypto API** for hashing
- **CesiumJS/Leaflet** for visualization

The "chain" is just each entry storing the hash of the previous entry. Simple, effective, free.

---

## Deployment

### GitHub Pages (Free)

1. Fork/create repo
2. Upload these 5 files
3. Enable Pages in Settings
4. Done

### Netlify Drop (Free)

1. Go to netlify.com
2. Drag & drop the folder
3. Get instant URL

### Local

Just open `index.html` in any modern browser.

---

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Requires WebGL (for 3D) and IndexedDB.

---

## Data Structure

```json
{
  "id": 1,
  "hash": "sha256_of_file",
  "filename": "photo.jpg",
  "location": { "lat": 40.71, "lng": -74.00 },
  "risk": 3,
  "description": "Power outage",
  "timestamp": 1709164800000,
  "previousHash": "hash_of_previous_entry"
}
```

---

## Security

- **Files never leave your browser** — hashing happens client-side
- **Tamper-evident** — break the chain, detection is immediate
- **Local only** — clear browser data = lose ledger (backup with Export)
- **Public anchors** — publish monthly hashes for external proof

---

## Future: Blockchain Integration

Phase 2 may add:
- IPFS for distributed file storage
- Optional blockchain anchoring
- Peer-to-peer sync

Phase 1 is intentionally simple: **just works, costs $0.**

---

## License

MIT — Use freely, modify freely, distribute freely.

---

**Map. Hash. Verify.**
