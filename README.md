## Hi, I'm Jay 👋
 
**M.S. Computer Science and Engineering @ Santa Clara University** (graduating May 2027) · I work where software meets hardware: FPGA acceleration, embedded firmware, OS kernels, and production backend systems.
 
Working across both has taught me that the biggest performance gains often come from rethinking where software and hardware meet, not from tuning either one in isolation.
 
### 🔬 FPGA Acceleration & Research
 
📄 **[An FPGA-Based CNN Accelerator Architecture Using Line-Buffer Layer Fusion for ADAS Applications](https://doi.org/10.5281/zenodo.22065607)**: first-author paper accepted to **IEEE MCSoC-2026** (with Prof. Radhika S. Grover)
 
- **Layer fusion:** Reordered convolution so each 2×2 max-pooling window's four inputs are produced back to back, removing the intermediate feature map and its buffer entirely
- **Results:** **3.29× fewer cycles** (13,096 → 3,978) and **2.53× fewer LUTs** than the same line-buffer design without fusion, with block RAM unchanged
- **On the board:** Classifies a traffic sign in **0.401 ms** and sustains **1,959 images/s** on a PYNQ-Z2 (Zynq-7020) over AXI DMA, bit-exact against the fixed-point reference; timing closes at 132.1 MHz
- **Open source:** Hardware source, testbench, and evaluation scripts released on [Zenodo](https://doi.org/10.5281/zenodo.22065607)
**LeNet-5 on PYNQ-Z2:** Benchmarked three progressively optimized HLS designs against an ARM CPU baseline. The deployed `ap_fixed<16,8>` design runs inference **57.78× faster** than software (20.67 ms vs 1,194 ms) at identical classification accuracy, in 26,892 LUTs and 29 DSPs.
- Moved a PIPELINE pragma from an outer to the innermost FC loop, cutting LUT usage about **100×** so the design fit the device
- Traced a silent misclassification to one FC1 accumulator overflowing its range and fixed it with wide `ap_fixed<32,16>` accumulation
### ⚙️ Embedded Systems & Operating Systems
 
- **Smart Parcel Locker (in progress, team of two):** STM32 Cortex-M4 + FreeRTOS. It detects packages with a ToF sensor and unlocks with an NFC phone token. I own the RTOS architecture and bring-up, the WiFi link to the phone, lock and alarm control, robustness (watchdog, per-state timeouts, I2C error recovery), and power tuning with tickless idle
- **Real-Time Firmware:** Interrupt-driven FreeRTOS temperature monitor with deferred ISR processing via binary semaphore, a mutex-protected threshold, and zero-timeout queues, losing **no readings** during alert handling. A 3-task accelerometer classifier sends 50-sample windows as single queue items, cutting model wakeups **50×**
- **Trace-Driven Debugging:** Used ARM SWV trace to catch a UART call silently returning `HAL_BUSY` (task runs of just **3.4 µs**) and a **100 → 160 ms** period drift fixed with `vTaskDelayUntil`; confirmed a rate-monotonic task set at 70% utilization against the 82.8% bound
- **xv6 Kernel (C, RISC-V, QEMU):** Added system calls for process, syscall, and free-page statistics with lock-protected kernel traversal and a `copyout` that rejects invalid pointers; built lottery and stride schedulers selectable at build time, passing all 53 xv6 usertests under each; added kernel-level threads via `clone()` with a user-level thread library and locks
- **Linux eBPF (in progress):** Debugging and extending an eBPF LSM file-access policy loaded into a live Linux kernel
### 🧪 Chip Design, DFT & Verification
 
- **Synthesis & Timing:** Synthesized RTL to SAED 32nm cells with Synopsys Design Compiler (`compile_ultra`), with clock constraints, I/O delays, and fanout limits; verified timing closure with STA
- **Scan & ATPG:** Inserted **160 scan flops** with Synopsys TestMAX DFT for **97.45% test coverage**; generated ATPG patterns reaching **90.51% fault coverage with 62 patterns**
- **Test Compression & BIST:** Evaluated 2:1, 4:1, and 8:1 scan compression tradeoffs; studied BIST, MBIST, and JTAG boundary scan
- **Functional Verification:** UVM-style SystemVerilog testbenches (driver, monitor, scoreboard) with constrained-random stimulus, SVA assertions, and functional coverage
### 💻 Production Software
 
**4+ years shipping production systems** across enterprise retail, utility billing, and AI products.
 
- **AI Backend @ fAIshion.ai:** Cut virtual try-on image generation from **40 s to 15 s** and raised the success rate to **100%** by migrating from a self-hosted ComfyUI pipeline to Gemini 2.5 Flash Image; built multi-provider failover in TypeScript/Next.js; migrated production MongoDB to Atlas with zero data loss
- **Utility Billing @ Itineris:** Shipped **100+ features across 20 releases with zero rollbacks** on a Dynamics 365 billing platform serving NYC DEP; cut deployment time from **45 to 10 minutes** with Python and PowerShell automation
- **Enterprise Retail:** Built and supported API integrations and data pipelines (C#/.NET, Java, SQL) for order-fulfillment systems behind Under Armour, Michael Kors, and Skechers
- **ML Research & Hackathons:** Built Python evaluation pipelines for multilingual LLM-text detection across 1M+ reviews with an Amazon Applied Scientist. **[Catch](https://devpost.com/software/catch-sojatf)** won the **AI-track Graduate Prize at AWS x INRIX Hack 2025**: real-time fall detection with YOLOv8-pose at 30+ FPS, cutting false positives 60%
### 🎯 Open To
 
`Systems Engineering` · `Embedded / Firmware Engineering` · `FPGA Engineering` · `Software Engineering` · `AI Infrastructure`
 
### 📚 Now & Next
 
Embedded Systems · Advanced Operating Systems *(this quarter)* · VLSI Design I *(next quarter)*
 
### 🛠️ Tech Stack
 
**Languages**
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![SystemVerilog](https://img.shields.io/badge/SystemVerilog-1A1A2E?style=for-the-badge) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logoColor=white)
 
**Hardware & FPGA**
![Vitis HLS](https://img.shields.io/badge/Vitis%20HLS-CC0033?style=for-the-badge&logo=amd&logoColor=white) ![Vivado](https://img.shields.io/badge/Vivado-AA0000?style=for-the-badge&logo=amd&logoColor=white) ![PYNQ](https://img.shields.io/badge/PYNQ-8A2BE2?style=for-the-badge) ![AXI](https://img.shields.io/badge/AXI%20Protocol-004466?style=for-the-badge) ![Synopsys](https://img.shields.io/badge/Synopsys%20DC%2FTestMAX-5A2D82?style=for-the-badge) ![UVM](https://img.shields.io/badge/UVM-2F4858?style=for-the-badge)
 
**Embedded & OS**
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-3D8B37?style=for-the-badge) ![STM32](https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white) ![ARM Cortex-M4](https://img.shields.io/badge/ARM%20Cortex--M4-0091BD?style=for-the-badge&logo=arm&logoColor=white) ![RISC-V](https://img.shields.io/badge/RISC--V-283272?style=for-the-badge&logo=riscv&logoColor=white) ![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=for-the-badge&logo=qemu&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
 
**Cloud & Backend**
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
 
### 📫 Reach Me
 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/j9yim) [![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:jayim1996@outlook.com) [![Zenodo](https://img.shields.io/badge/Zenodo-Paper%20Source-1682D4)](https://doi.org/10.5281/zenodo.22065607)
