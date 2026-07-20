## Hi, I'm Jay 👋

**Computer Engineering M.S. @ Santa Clara University** · I work across the full stack — from **RTL, DFT, and FPGA acceleration** to **backend systems and ML pipelines**

I'm interested in the space where hardware and software meet: accelerating ML on FPGAs, making silicon testable, verifying complex digital designs, and building reliable production systems. 4+ years of industry software experience, now going deep on the hardware side.
 
### 🔬 FPGA & Acceleration
**FPGA Research Assistant @ SCU** — re-architected a LeNet-5 CNN accelerator into a streaming HLS dataflow design on a Xilinx Zynq-7020, cutting inference latency **~12x** (14.5M → 1.2M cycles) via pipelining, memory partitioning, and `ap_fixed` quantization — verified against a golden reference model.
- **HLS Optimization** — Loop unrolling, pipelining, and array partitioning under a hard 10ns timing target; identified 16-bit fixed-point as the minimum width preserving classification accuracy
- **HW/SW Co-Design** — AXI4-Lite memory-mapped and streaming interfaces bridging FPGA fabric to ARM host with Vitis HLS + PYNQ; benchmarked ML inference speedup vs. CPU

### 🧪 DFT & Verification 
- **Synthesis & Timing** — Synthesized RTL to SAED 32nm RVT cells with Synopsys Design Compiler (`compile_ultra`); applied clock constraints, I/O delays, and fanout limits, verifying timing closure via STA
- **Scan & Test Coverage** — Inserted **160 scan flops** achieving **97.45% test coverage** with TestMAX DFT; analyzed SRAM DFT structure impact on coverage
- **ATPG & Compression** — Reached **90.51% fault coverage with 62 patterns**; evaluated 2:1 / 4:1 / 8:1 test compression tradeoffs across stuck-at modeling, BIST, MBIST, and JTAG/boundary scan
- **Functional Verification** — UVM-style SystemVerilog testbenches with modular VIP components (driver, monitor, scoreboard), constrained-random stimulus, SVA assertions, and functional coverage sign-off

### 💻 Software
**4+ years shipping production systems** for enterprise clients including Under Armour, Michael Kors, and Skechers.
- **Backend Engineering** — Built a virtual try-on microservice @ fAIshion.ai (Gemini 2.5 Flash, ~15s processing, 100% success rate) with a TypeScript/Next.js high-availability fallback system
- **Enterprise Integration** — API integrations and data pipelines (C#/.NET, Java, SQL) for Dynamics 365 and order-fulfillment platforms; Kafka-based monitoring that cut unplanned downtime **40%**
- **DevOps & Cloud** — Azure DevOps CI/CD pipelines reducing deployment time 40%; AWS-backed architectures with 99.9% uptime
- **ML & Research** — LLM evaluation frameworks (deception detection across 1M+ reviews with an Amazon Applied Scientist); YOLOv8 real-time pose detection that won the **AWS x INRIX Hack 2025** 🏆
 
### 🎯 Open To
`DFT Engineering` · `FPGA Engineering` · `Software Engineering` · `ML Infrastructure`
 
### 📚 Up Next
Embedded Systems · VLSI Design I *(next quarter)*
 
### 📫 Reach Me + Socials:
[![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/im.jeonghun.1) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/j9y_im) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/j9yim) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:jayim1996@outlook.com) 

## 💻 Tech Stack:
### Languages
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![SystemVerilog](https://img.shields.io/badge/SystemVerilog-1A1A2E?style=for-the-badge) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logoColor=white) ![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white) ![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)
 
### Hardware & FPGA
![AMD](https://img.shields.io/badge/AMD%20Xilinx-%23000000.svg?style=for-the-badge&logo=amd&logoColor=white) ![Vivado](https://img.shields.io/badge/Vivado-AA0000?style=for-the-badge&logo=amd&logoColor=white) ![Vitis HLS](https://img.shields.io/badge/Vitis%20HLS-CC0033?style=for-the-badge&logo=amd&logoColor=white) ![PYNQ](https://img.shields.io/badge/PYNQ-8A2BE2?style=for-the-badge) ![UVM](https://img.shields.io/badge/UVM-2F4858?style=for-the-badge) ![Synopsys](https://img.shields.io/badge/Synopsys%20DC%2FTestMAX-5A2D82?style=for-the-badge) ![AXI](https://img.shields.io/badge/AXI%20Protocol-004466?style=for-the-badge)
### Backend & Frameworks
![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) ![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white) ![Dynamics 365](https://img.shields.io/badge/Dynamics%20365-0B53CE?style=for-the-badge&logo=microsoft&logoColor=white)
 
### ML / AI
![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-FFD21E?style=for-the-badge&logoColor=black) ![YOLOv8](https://img.shields.io/badge/YOLOv8-00FFFF?style=for-the-badge&logoColor=black) ![LLMs](https://img.shields.io/badge/LLMs-FF6B6B?style=for-the-badge) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
 
### Cloud & DevOps
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Azure DevOps](https://img.shields.io/badge/Azure%20DevOps-0078D7?style=for-the-badge&logo=azuredevops&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka) ![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
 
### Databases
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) ![AmazonDynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=for-the-badge&logo=Amazon%20DynamoDB&logoColor=white)

## 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api?username=ImJ9y&theme=swift&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://streak-stats.demolab.com/?user=ImJ9y&theme=swift&hide_border=false)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=ImJ9y&theme=swift&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

## ✍️ Quote of day:
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

---
<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
