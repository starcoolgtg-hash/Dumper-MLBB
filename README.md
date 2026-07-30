# Dumper-MLBB

A powerful native dumper library designed for Mobile Legends: Bang Bang (MLBB) binary analysis and reverse engineering research.

---

## 📌 Features

* **Native Hooking & Dumping**: Injects directly via native `.so` library.
* **Easy Integration**: Simple Smali injection into the application lifecycle.
* **Lightweight**: Optimized shared object implementation (`libStarcool_unity.so`).

---

## 🚀 Usage Guide

To load the dumper library into the target application, inject the following Smali code snippet into the main Activity or entry point (e.g., `onCreate` or static initializer):

```smali
const-string v0, "Starcool_unity"
invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V
