---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---


## <span style="color:#063c72">CRIBA</span>
CRIBA is an open-source framework that simplifies the exploration, analysis, and comparison of I/O patterns for Linux cryptographic ransomware. It is built on top of DIO, a generic tool for observing and diagnosing the I/O interactions between applications and in-kernel POSIX storage systems.<br>
<a href="https://github.com/dsrhaslab/criba">
    <img src="https://img.shields.io/badge/dsrhaslab/criba-black?stype=plastic&logo=github&logoColor=white&labelColor=blue"/>
</a>
<hr>


## <span style="color:#063c72">DIO</span>
DIO is a generic tool for observing and diagnosing applications storage I/O. It is designed to be used by applications developers and users to understand how applications interact with storage systems. By combining system call tracing, through eBPFs, with a customizable data analysis and visualization pipeline, DIO provide non-intrusive and comprehensive I/O diagnosis for applications using in-kernel POSIX storage systems (e.g., ext4, linux block device).<br>
<a href="https://github.com/dsrhaslab/dio">
    <img src="https://img.shields.io/badge/dsrhaslab%2Fdio-black?style=plastic&logo=github&logoColor=white&labelColor=blue"/>
</a>
<a href="https://dio-tool.netlify.app">
    <img src="https://img.shields.io/badge/dio--tool.netlify.app-black?style=plastic&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxOCAxOCI+PHBhdGggZD0iTTkgM2E2IDYgMCAwIDAgMCAxMmE2IDYgMCAwIDAgMCAtMTJaTTcuNiA0LjJhNSA1IDAgMCAwIDAgOS42YTggOCAwIDAgMSAwIC05LjZaTTEwLjQgNC4yYTUgNSAwIDAgMSAwIDkuNmE4IDggMCAwIDAgMCAtOS42Wk05IDQuMWE3IDcgMCAwIDAgMCA5LjhhNyA3IDAgMCAwIDAgLTkuOCIgc3R5bGU9ImZpbGwtcnVsZTogZXZlbm9kZDsgZmlsbDogd2hpdGUiIC8+PHBhdGggc3R5bGU9Im9wYWNpdHk6IDAuNTsgZmlsbDogd2hpdGUiIGQ9Ik00LjEgOGE1IDUgMCAwIDEgMC4zMSAtMWgxLjg1YTggOCAwIDAgMCAtMC4yIDFaTTEzLjkgOGE1IDUgMCAwIDAgLTAuMzEgLTFoLTEuODVhOCA4IDAgMCAxIDAuMiAxWk00LjEgMTBhNSA1IDAgMCAwIDAuMzEgMWgxLjg1YTggOCAwIDAgMSAtMC4yIC0xWk0xMy45IDEwYTUgNSAwIDAgMSAtMC4zMSAxaC0xLjg1YTggOCAwIDAgMCAwLjIgLTFaTTcuMDcgOGE3IDcgMCAwIDEgMC4yMiAtMWgzLjQyYTcgNyAwIDAgMSAwLjIyIDFaTTcuMDcgMTBhNyA3IDAgMCAwIDAuMjIgMWgzLjQyYTcgNyAwIDAgMCAwLjIyIC0xWiIgLz48L3N2Zz4=&labelColor=purple" alt="Website"/>
</a>
<hr>

## <span style="color:#063c72">CaT</span>
CaT is a black-box content-aware tracing and analysis framework. It analyzes distributed systems in a non-intrusive way, highlighting how their components interact with each other and how data flows through the system. Its design enables the capture of detailed information related to I/O network and disk events, such as the context of the request and the data processed by the event. With this information, CaT proposes an analysis of the event’s content based on their similarity, allowing the detection of data flow patterns that are not visible when inspecting only the context of events.<br>
<a href="https://github.com/dsrhaslab/cat">
    <img src="https://img.shields.io/badge/dsrhaslab%2Fcat-black?style=plastic&logo=github&logoColor=white&labelColor=blue"/>
</a>
<hr>

## <span style="color:#063c72">TrustFS</span>
TrustFS is an open-source programmable, and modular stackable file system framework for implement- ing secure content-aware storage functionalities over hardware-assisted trusted execution environments. TrustFS extends the original SafeFS architecture to provide the isolated execution guarantees of Intel SGX.<br>
<a href="https://github.com/taniaesteves/TrustFS">
    <img src="https://img.shields.io/badge/taniaesteves%2FTrustFS-black?style=plastic&logo=github&logoColor=white&labelColor=blue"/>
</a>
<hr>
