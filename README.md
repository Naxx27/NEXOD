# NEXOD – Next‑Gen Operating System Device

🇬🇧 [This README is available in English, German and Russian.](#-english-version)

🇩🇪 [Diese README ist auf Englisch, Deutsch und Russisch verfügbar.](#-deutsche-version)

🇷🇺 [Этот README доступен на английском, немецком и русском языках.](#-русская-версия)

---

# 🇬🇧 English Version

## Overview

**NEXOD (Next‑Gen Operating System Device)** is a new hardware–firmware architecture that replaces the traditional BIOS/UEFI model with a powerful pre‑OS control layer.  
It initializes, partitions, and manages hardware resources *before* any operating system starts — enabling multiple OS instances to run natively and in parallel on the same machine.

Unlike hypervisors, bootloaders, or virtualization layers, NEXOD is **not software running on top of an OS**.  
It is a **new hardware execution model + a new firmware architecture**, designed to control CPU domains, GPU contexts, PCIe routing, memory isolation, and device arbitration at the lowest possible level.

After hardware initialization, NEXOD launches one or more operating systems based on user selection or predefined profiles.

**Author:** Nexx (JQ)  
**Status:** Concept Architecture / Research Draft  
**License:** See LICENSE file

---

## Boot Process Overview

NEXOD replaces the traditional BIOS/UEFI boot chain.  
It becomes the first execution layer after power‑on:

1. Power‑on → NEXOD firmware starts  
2. NEXOD initializes hardware domains  
3. CPU, GPU, PCIe, memory and devices are partitioned  
4. OS instances are launched in parallel  
5. Each OS believes it owns the hardware exclusively  

More details:  
👉 `docs/boot_process.md`

---

## Key Components

### 🔹 Dual‑Domain CPU Execution  
Hardware‑level CPU partitioning with isolated register sets, interrupts, page tables, and privilege levels.

### 🔹 Multi‑Context GPU  
Parallel GPU hardware contexts for multiple OS domains without driver conflicts.

### 🔹 PCIe Multiplexing & Arbitration  
Dynamic and safe device sharing between OS domains at native performance.

### 🔹 NEXOD Firmware Layer  
A next‑generation BIOS/UEFI replacement that boots and manages multiple OS domains simultaneously.

### 🔹 Security & Isolation  
Strict hardware‑level separation of memory, devices, interrupts, and DMA.

---

## Documentation

All documents are located in the `docs/` directory:

- [Abstract](docs/abstract.md) ✅
- [Architecture Overview](docs/architecture_overview.md)  
- [Boot Process](docs/boot_process.md)  
- [CPU Model](docs/nexod_cpu_model.md)  
- [GPU Model](docs/nexod_gpu_model.md)  
- [PCIe Model](docs/nexod_pcie_model.md)  
- [Firmware Model](docs/nexod_firmware_model.md)  
- [Use Cases](docs/use_cases.md)  
- [Comparison to Existing Technologies](docs/comparison_existing_tech.md)  
- [Future Outlook](docs/future_outlook.md)

*(These files will be added step by step.)*

---

## Goals of the Project

- Define a new hardware‑firmware architecture  
- Replace BIOS/UEFI with a multi‑OS control layer  
- Enable native parallel OS execution  
- Overcome hypervisor limitations  
- Provide safe device sharing without virtualization  
- Inspire research in system architecture and hardware design

---

## Contribution

This project is in conceptual development.  
Feedback and discussion are welcome.

---

# 🇩🇪 Deutsche Version

## Übersicht

**NEXOD (Next‑Gen Operating System Device)** ist eine neue Hardware‑/Firmware‑Architektur, die das klassische BIOS/UEFI‑Modell ersetzt.  
NEXOD fungiert als leistungsfähige **Pre‑OS‑Kontrollschicht**, die Hardware initialisiert, partitioniert und verwaltet, *bevor* ein Betriebssystem startet — und ermöglicht so die native, parallele Ausführung mehrerer Betriebssysteme auf derselben Maschine.

Im Gegensatz zu Hypervisoren, Bootloadern oder Virtualisierungslayern ist NEXOD **keine Software, die auf einem OS läuft**.  
Es ist ein **neues Hardware‑Ausführungsmodell + eine neue Firmware‑Architektur**, die CPU‑Domänen, GPU‑Kontexte, PCIe‑Routing, Speicherisolation und Gerätearbitration auf niedrigster Ebene kontrolliert.

Nach der Initialisierung startet NEXOD eine oder mehrere Betriebssysteme basierend auf Benutzerwahl oder Profilen.

**Autor:** Nexx (JQ)  
**Status:** Konzeptarchitektur / Forschungsentwurf  
**Lizenz:** Siehe LICENSE‑Datei

---

## Boot‑Prozess Übersicht

NEXOD ersetzt die klassische BIOS/UEFI‑Bootkette.  
Es ist die erste Ausführungsschicht nach dem Einschalten:

1. Einschalten → NEXOD‑Firmware startet  
2. NEXOD initialisiert Hardware‑Domänen  
3. CPU, GPU, PCIe, Speicher und Geräte werden partitioniert  
4. OS‑Instanzen werden parallel gestartet  
5. Jede OS‑Instanz glaubt, sie besitze die Hardware exklusiv  

Mehr Details:  
👉 `docs/boot_process.md`

---

## Hauptkomponenten

### 🔹 Dual‑Domain CPU Execution  
Hardware‑basierte CPU‑Partitionierung mit isolierten Registern, Interrupts, Page‑Tables und Privilegstufen.

### 🔹 Multi‑Context GPU  
Parallele GPU‑Hardware‑Kontexte für mehrere OS‑Domänen ohne Treiberkonflikte.

### 🔹 PCIe‑Multiplexing & Arbitration  
Dynamisches und sicheres Teilen von PCIe‑Geräten bei nativer Performance.

### 🔹 NEXOD‑Firmware  
Ein BIOS/UEFI‑Nachfolger, der mehrere Betriebssysteme gleichzeitig booten und verwalten kann.

### 🔹 Sicherheits‑ und Isolationsmodell  
Strikte hardwarebasierte Trennung von Speicher, Geräten, Interrupts und DMA.

---

## Dokumentation

Alle Dokumente befinden sich im Ordner `docs/`:

- [Abstract](docs/abstract.md) ✅
- [Architekturübersicht](docs/architecture_overview.md)  
- [Boot‑Prozess](docs/boot_process.md)  
- [CPU‑Modell](docs/nexod_cpu_model.md)  
- [GPU‑Modell](docs/nexod_gpu_model.md)  
- [PCIe‑Modell](docs/nexod_pcie_model.md)  
- [Firmware‑Modell](docs/nexod_firmware_model.md)  
- [Anwendungsfälle](docs/use_cases.md)  
- [Vergleich mit bestehenden Technologien](docs/comparison_existing_tech.md)  
- [Zukunftsausblick](docs/future_outlook.md)

*(Diese Dateien werden Schritt für Schritt hinzugefügt.)*

---

## Ziele des Projekts

- Definition einer neuen Hardware‑/Firmware‑Architektur  
- Ersatz von BIOS/UEFI durch eine Multi‑OS‑Kontrollschicht  
- Native parallele OS‑Ausführung  
- Überwindung klassischer Hypervisor‑Grenzen  
- Sicheres Teilen von Geräten ohne Virtualisierung  
- Förderung von Forschung im Bereich System‑ und Hardwarearchitektur

---

## Beiträge

Das Projekt befindet sich in konzeptioneller Entwicklung.  
Feedback und Diskussionen sind willkommen.

---

# 🇷🇺 Русская версия

## Обзор

**NEXOD (Next‑Gen Operating System Device)** — это новая аппаратно‑прошивочная архитектура, заменяющая классическую модель BIOS/UEFI.  
NEXOD работает как мощный **пред‑ОС управляющий слой**, который инициализирует, разделяет и контролирует оборудование *до* запуска любой операционной системы — обеспечивая нативный параллельный запуск нескольких ОС на одном устройстве.

В отличие от гипервизоров, загрузчиков или виртуализационных слоёв, NEXOD — это **не программа поверх ОС**.  
Это **новая аппаратная модель выполнения + новая архитектура прошивки**, управляющая CPU‑доменами, GPU‑контекстами, PCIe‑маршрутизацией, изоляцией памяти и арбитражем устройств на самом низком уровне.

После инициализации NEXOD запускает одну или несколько ОС в зависимости от выбора пользователя или профилей.

**Автор:** Nexx (JQ)  
**Статус:** Концептуальная архитектура / исследовательский проект  
**Лицензия:** См. LICENSE

---

## Обзор процесса загрузки

NEXOD заменяет традиционную цепочку BIOS/UEFI.  
Это первый слой выполнения после включения питания:

1. Включение → запускается прошивка NEXOD  
2. NEXOD инициализирует аппаратные домены  
3. CPU, GPU, PCIe, память и устройства разделяются  
4. ОС запускаются параллельно  
5. Каждая ОС считает, что владеет оборудованием полностью  

Подробнее:  
👉 `docs/boot_process.md`

---

## Ключевые компоненты

### 🔹 Dual‑Domain CPU Execution  
Аппаратное разделение CPU с изолированными регистрами, прерываниями, таблицами страниц и уровнями привилегий.

### 🔹 Multi‑Context GPU  
Параллельные аппаратные GPU‑контексты для нескольких ОС без конфликтов драйверов.

### 🔹 PCIe Multiplexing & Arbitration  
Динамическое и безопасное совместное использование PCIe‑устройств с нативной производительностью.

### 🔹 Прошивка NEXOD  
Наследник BIOS/UEFI, способный загружать и управлять несколькими ОС одновременно.

### 🔹 Модель безопасности и изоляции  
Строгая аппаратная изоляция памяти, устройств, прерываний и DMA.

---

## Документация

Все документы находятся в каталоге `docs/`:

- [Abstract](docs/abstract.md) ✅
- [Architecture Overview](docs/architecture_overview.md)  
- [Boot Process](docs/boot_process.md)  
- [CPU Model](docs/nexod_cpu_model.md)  
- [GPU Model](docs/nexod_gpu_model.md)  
- [PCIe Model](docs/nexod_pcie_model.md)  
- [Firmware Model](docs/nexod_firmware_model.md)  
- [Use Cases](docs/use_cases.md)  
- [Comparison to Existing Technologies](docs/comparison_existing_tech.md)  
- [Future Outlook](docs/future_outlook.md)

*(Эти файлы будут добавляться постепенно.)*

---

## Цели проекта

- Определение новой аппаратно‑прошивочной архитектуры  
- Замена BIOS/UEFI многодоменным управляющим слоем  
- Нативный параллельный запуск нескольких ОС  
- Преодоление ограничений гипервизоров  
- Безопасное совместное использование устройств без виртуализации  
- Стимулирование исследований в области архитектуры систем и оборудования

---

## Участие

Проект находится на стадии концептуальной разработки.  
Идеи и обсуждения приветствуются.
