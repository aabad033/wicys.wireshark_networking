# Module 1: Foundations & Your First Capture

### 1. What is Networking?
[cite_start]Networking is the process of connecting computers (or other devices) to exchange data[cite: 2]. [cite_start]For devices to communicate, they require a guide or standard to ensure they are speaking the same "language"[cite: 3].



[cite_start]We utilize the **5-Layer Model** to break down these communication standards[cite: 4]:
* [cite_start]**Application**: The user interface/protocol (e.g., your browser)[cite: 4].
* [cite_start]**Transport**: Handles end-to-end communication[cite: 5].
* **Network**: Manages routing across the globe.
* [cite_start]**Data Link**: Communication between local neighbors[cite: 7].
* [cite_start]**Physical**: The actual bits on the wire[cite: 6].

---

### 2. Pre-Flight Checklist
Before we start capturing traffic, we need to prepare the environment to ensure data is visible:

* [cite_start]**Install Wireshark**: [Download the latest version here](https://www.wireshark.org/#download)[cite: 1].
* [cite_start]**Disable VPNs**: Remove any active VPN you currently have, as this will cause capture issues[cite: 8].
* **Disable QUIC/HTTP3**: Modern browsers encrypt traffic using QUIC/HTTP3 by default. [cite_start]Follow [this guide](https://techysnoop.com/disable-quic-protocol-in-chrome-edge-firefox/) to disable it so the packets remain readable for this lab[cite: 9].

---

### 3. Capture Walkthrough
[cite_start]Now, let's see the 5-layer model in action[cite: 12].

**Step 1: Launch & Select**
* [cite_start]Open Wireshark[cite: 9].
* Select a capture interface. [cite_start]Choose the one that shows a **bar graph reacting**, as this indicates it is actively capturing data[cite: 10].

**Step 2: Generate Traffic**
* [cite_start]Once in the capture window, you can manage the session using the options at the top (Stop, Start, Adjust)[cite: 11].
* [cite_start]Open your browser and visit: [http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html](http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html)[cite: 13].
* Stop the capture once the page loads to begin your analysis.

**Step 3: Analyze & Filter**
* [cite_start]**Why HTTP?** This link uses `http://`, which does **not** encrypt data (unlike `https://`), allowing us to see the connection details[cite: 14].
* [cite_start]**Filter**: Click the search bar at the top and enter `http` to isolate the packages sent using that protocol[cite: 15].
* [cite_start]**Troubleshooting**: If you do not see packets, try redoing the steps or use the provided example file by selecting `File > Open`[cite: 16, 17].
