# Module 1: Foundations & Your First Capture

### 1. What is Networking?
Networking is the process of connecting computers (or other devices) to exchange data. For devices to communicate, they require a guide or standard to ensure they are speaking the same "language".

[Image of 5-layer network model]

We utilize the **5-Layer Model** to break down these communication standards:
* **Application**: The user interface/protocol (e.g., your browser).
* **Transport**: Handles end-to-end communication.
* **Network**: Manages routing across the globe.
* **Data Link**: Communication between local neighbors.
* **Physical**: The actual bits on the wire.

---

### 2. Pre-Flight Checklist
Before we start capturing traffic, we need to prepare the environment to ensure data is visible:

* **Install Wireshark**: [Download the latest version here](https://www.wireshark.org/#download).
* **Disable VPNs**: Remove any active VPN you currently have, as this will cause capture issues.
* **Disable QUIC/HTTP3**: Modern browsers encrypt traffic using QUIC/HTTP3 by default. Follow [this guide](https://techysnoop.com/disable-quic-protocol-in-chrome-edge-firefox/) to disable it so the packets remain readable for this lab.

---

### 3. Capture Walkthrough
Now, let's see the 5-layer model in action.

**Step 1: Launch & Select**
* Open Wireshark.
* Select a capture interface. Choose the one that shows a **bar graph reacting**, as this indicates it is actively capturing data.

**Step 2: Generate Traffic**
* Once in the capture window, you can manage the session using the options at the top (Stop, Start, Adjust).
* Open your browser and visit: [http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html](http://gaia.cs.umass.edu/wireshark-labs/INTRO-wireshark-file1.html).
* Stop the capture once the page loads to begin your analysis.

**Step 3: Analyze & Filter**
* **Why HTTP?** This link uses `http://`, which does **not** encrypt data (unlike `https://`), allowing us to see the connection details.
* **Filter**: Click the search bar at the top and enter `http` to isolate the packages sent using that protocol.
* **Troubleshooting**: If you do not see packets, try redoing the steps or use the provided example file by selecting `File > Open`.
