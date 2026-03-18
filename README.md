# NEXOD – Next‑Gen Operating System Device

This README is available in English, German and Russian.  
README ist auf Englisch, Deutsch und Russisch verfügbar.  
README доступен на английском, немецком и русском языках.

---

# 🇬🇧 English Version

## Overview

**NEXOD (Next‑Gen Operating System Device)** is a conceptual hardware‑control architecture designed to run multiple operating systems in parallel on the same machine.  
Unlike traditional hypervisors or bootloaders, NEXOD acts as a **primary control layer** that boots *before* any operating system and manages hardware resources at the lowest level.

NEXOD initializes CPU domains, GPU queues, PCIe arbitration, memory isolation, and firmware abstraction.  
After initialization, NEXOD launches one or multiple OS instances based on user selection or predefined profiles.

**Author:** Nexx (JQ)  
**Status:** Concept Architecture / Research Draft  
**License:** See LICENSE file

---

## Boot Process Overview

NEXOD boots first and acts as the master control layer.  
It initializes hardware domains, assigns resources, and then starts one or multiple operating systems in parallel.  
Users may choose OS instances through a boot menu or rely on automatic profiles.

A detailed explanation is available in:  
👉 `docs/boot_process.md`

---

## Key Components

### 🔹 CPU Partitioning Layer  
Creates isolated CPU domains for each OS instance, supporting static or dynamic core allocation.

### 🔹 GPU Multiplexing Layer  
Provides virtual GPU queues that allow multiple OS domains to share GPU resources without driver conflicts.

### 🔹 PCIe Multiplexing & Arbitration Layer  
Ensures safe and conflict‑free access to PCIe devices such as NVMe, USB controllers, NICs, and more.

### 🔹 Firmware Abstraction Layer  
Separates hardware initialization from OS domains and prevents firmware‑level interference.

### 🔹 Security & Isolation Model  
Guarantees strict separation between OS instances, preventing memory, device, or data conflicts.

---

## Documentation

All detailed documents are located in the `docs/` directory:

- [Abstract](docs/abstract.md)  
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

- Explore new hardware‑level virtualization concepts  
- Provide a clean, modular architecture for multi‑OS systems  
- Overcome limitations of traditional hypervisors  
- Enable safe device sharing without corruption  
- Inspire research and discussion in system architecture communities

---

## Contribution

This project is currently in conceptual development.  
Feedback, ideas, and discussions are welcome.

---

# 🇩🇪 Deutsche Version

## Übersicht

**NEXOD (Next‑Gen Operating System Device)** ist eine konzeptionelle Hardware‑Kontrollarchitektur, die mehrere Betriebssysteme parallel auf derselben Maschine ausführen kann.  
Im Gegensatz zu klassischen Hypervisoren oder Bootloadern fungiert NEXOD als **primäre Kontrollschicht**, die *vor* jedem Betriebssystem startet und die Hardware auf niedrigster Ebene verwaltet.

NEXOD initialisiert CPU‑Domänen, GPU‑Queues, PCIe‑Arbitration, Speicherisolation und Firmware‑Abstraktion.  
Nach der Initialisierung startet NEXOD eine oder mehrere OS‑Instanzen basierend auf Benutzerwahl oder vordefinierten Profilen.

**Autor:** Nexx (JQ)  
**Status:** Konzeptarchitektur / Forschungsentwurf  
**Lizenz:** Siehe LICENSE‑Datei

---

## Boot‑Prozess Übersicht

NEXOD startet zuerst und fungiert als Master‑Kontrollschicht.  
Es initialisiert Hardware‑Domänen, weist Ressourcen zu und startet anschließend eine oder mehrere Betriebssysteme parallel.  
Der Benutzer kann OS‑Instanzen über ein Boot‑Menü auswählen oder automatische Profile nutzen.

Eine ausführliche Erklärung befindet sich in:  
👉 `docs/boot_process.md`

---

## Hauptkomponenten

### 🔹 CPU‑Partitionierungs‑Layer  
Erstellt isolierte CPU‑Domänen für jede OS‑Instanz, mit statischer oder dynamischer Kernzuweisung.

### 🔹 GPU‑Multiplexing‑Layer  
Ermöglicht mehreren OS‑Domänen die sichere gemeinsame Nutzung der GPU ohne Treiberkonflikte.

### 🔹 PCIe‑Multiplexing & Arbitration Layer  
Sorgt für konfliktfreien Zugriff auf PCIe‑Geräte wie NVMe, USB‑Controller oder Netzwerkkarten.

### 🔹 Firmware‑Abstraktions‑Layer  
Trennt die Hardware‑Initialisierung von den OS‑Domänen und verhindert Firmware‑Konflikte.

### 🔹 Sicherheits‑ und Isolationsmodell  
Garantiert strikte Trennung zwischen OS‑Instanzen und verhindert Speicher‑ oder Geräteinterferenzen.

---

## Dokumentation

Alle detaillierten Dokumente befinden sich im Ordner `docs/`:

- [Abstract](docs/abstract.md)  
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

- Erforschung neuer Hardware‑Virtualisierungskonzepte  
- Saubere, modulare Architektur für Multi‑OS‑Systeme  
- Überwindung klassischer Hypervisor‑Einschränkungen  
- Sicheres Teilen von Geräten ohne Datenkorruption  
- Anregung zu Forschung und Diskussion in der Systemarchitektur

---

## Beiträge

Das Projekt befindet sich derzeit in der konzeptionellen Entwicklung.  
Feedback, Ideen und Diskussionen sind willkommen.

---

# 🇷🇺 Русская версия

## Обзор

**NEXOD (Next‑Gen Operating System Device)** — это концептуальная архитектура управления оборудованием, предназначенная для одновременного запуска нескольких операционных систем на одном компьютере.  
В отличие от традиционных гипервизоров или загрузчиков, NEXOD действует как **основной управляющий слой**, который запускается *до* любой операционной системы и управляет аппаратными ресурсами на самом низком уровне.

NEXOD инициализирует CPU‑домены, GPU‑очереди, арбитраж PCIe, изоляцию памяти и абстракцию прошивки.  
После инициализации NEXOD запускает одну или несколько ОС в зависимости от выбора пользователя или заранее определённых профилей.

**Автор:** Nexx (JQ)  
**Статус:** Концептуальная архитектура / исследовательский проект  
**Лицензия:** См. файл LICENSE

---

## Обзор процесса загрузки

NEXOD загружается первым и действует как главный управляющий слой.  
Он инициализирует аппаратные домены, распределяет ресурсы и затем запускает одну или несколько операционных систем параллельно.  
Пользователь может выбрать ОС через меню загрузки или использовать автоматические профили.

Подробное описание доступно в:  
👉 `docs/boot_process.md`

---

## Ключевые компоненты

### 🔹 Слой разделения CPU  
Создаёт изолированные CPU‑домены для каждой ОС с поддержкой статического или динамического распределения ядер.

### 🔹 Слой мультиплексирования GPU  
Предоставляет виртуальные GPU‑очереди, позволяющие нескольким ОС безопасно использовать GPU без конфликтов драйверов.

### 🔹 Слой мультиплексирования и арбитража PCIe  
Обеспечивает безопасный и бесконфликтный доступ к устройствам PCIe, таким как NVMe, USB‑контроллеры, сетевые карты и др.

### 🔹 Слой абстракции прошивки  
Отделяет аппаратную инициализацию от доменов ОС и предотвращает конфликты на уровне прошивки.

### 🔹 Модель безопасности и изоляции  
Гарантирует строгую изоляцию между ОС и предотвращает конфликты памяти, устройств и данных.

---

## Документация

Все подробные документы находятся в каталоге `docs/`:

- [Abstract](docs/abstract.md)  
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

- Исследование новых концепций виртуализации на уровне оборудования  
- Создание чистой, модульной архитектуры для систем с несколькими ОС  
- Преодоление ограничений традиционных гипервизоров  
- Обеспечение безопасного совместного использования устройств  
- Стимулирование исследований и обсуждений в области системной архитектуры

---

## Участие

Проект находится на стадии концептуальной разработки.  
Приветствуются идеи, предложения и обсуждения.
