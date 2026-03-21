# NEXOD – Abstract  
🇬🇧 [*(This document is available in English, German and Russian.)*](#english-abstract) 
🇩🇪 [*(Dieses Dokument ist auf Englisch, Deutsch und Russisch verfügbar.)*](#deutsches-abstract) 
🇷🇺 [*(Этот документ доступен на английском, немецком и русском языках.)*](#-русский-abstract) 

---

# 🇬🇧 English Abstract

NEXOD (Next‑Gen Operating System Device) describes a new computer architecture
capable of running multiple operating systems natively and simultaneously on the
same hardware. Unlike virtualization or dual‑boot setups, each operating system
receives its own fully isolated hardware domain – without emulation, without
driver modifications, and without performance loss.

To enable this form of native parallelism, NEXOD introduces four new hardware concepts:

1. **Dual‑Domain‑Execution CPU**  
   A CPU capable of running two fully separated execution domains at the same time.
   Each domain has its own registers, interrupt tables, page tables, and privilege
   levels. Both operating systems run in parallel and each believes it is operating
   in true root mode – without any virtualization layer.

2. **Multi‑Context GPU**  
   A GPU capable of executing multiple real hardware contexts simultaneously.
   Each OS domain receives its own GPU registers, VRAM regions, and command queues.
   This allows multiple operating systems to perform rendering or compute tasks
   concurrently without blocking each other.

3. **PCIe Multiplexing Layer + Firmware Abstraction Layer (FAL)**  
   A new hardware‑firmware layer that dynamically and safely assigns PCIe devices
   to multiple operating systems in parallel.  
   The **Firmware Abstraction Layer (FAL)** handles PCIe routing, DMA isolation,
   interrupt separation, and device arbitration.  
   This layer is essential because traditional BIOS/UEFI cannot initialize or
   manage multi‑domain PCIe hardware.

4. **Dual‑OS Firmware Model**  
   A firmware capable of booting and managing two operating systems simultaneously.
   Each domain receives its own ACPI tables, interrupt routing, and hardware
   abstractions. The firmware initializes and controls both OS domains in parallel.

## New Boot Architecture (BIOS Replacement)

Because NEXOD relies on hardware that does not exist in current systems,
it also requires a **completely new boot architecture**.

NEXOD replaces BIOS/UEFI entirely and becomes the first component that runs after power‑on:

1. Power‑on → NEXOD firmware starts  
2. Hardware domains are initialized  
3. CPU/GPU/PCIe resources are partitioned  
4. Memory and interrupts are isolated  
5. Multiple operating systems are launched in parallel  

This new boot model is essential, because traditional BIOS/UEFI cannot initialize
or manage multi‑domain hardware.

## Vision

Through these components, NEXOD enables a new form of computing:
Windows, Linux, or other systems can run natively at the same time – visible on
multiple displays or instantly switchable via hotkey. Developers can test software
in parallel, users no longer need multiple devices, and modern hardware is utilized
fully for the first time.

---

# 🇩🇪 Deutsches Abstract

NEXOD (Next‑Gen Operating System Device) beschreibt eine neue Computerarchitektur,
die mehrere Betriebssysteme gleichzeitig nativ auf derselben Hardware ausführen kann.
Im Gegensatz zu Virtualisierung oder Dual‑Boot erhält jedes Betriebssystem eine
vollständig isolierte Hardware‑Domäne – ohne Emulation, ohne Treiberanpassungen
und ohne Performanceverlust.

Um diese Form der nativen Parallelität zu ermöglichen, definiert NEXOD vier neue Hardware‑Konzepte:

1. **Dual‑Domain‑Execution‑CPU**  
   Eine CPU, die zwei vollständig getrennte Ausführungsdomänen gleichzeitig
   betreiben kann. Jede Domäne besitzt eigene Register, Interrupt‑Tabellen,
   Page‑Tables und Privilegstufen. Beide Betriebssysteme laufen parallel und
   glauben jeweils, sie seien im echten Root‑Modus – ohne Virtualisierungsschicht.

2. **Multi‑Context‑GPU**  
   Eine GPU, die mehrere echte Hardware‑Kontexte gleichzeitig ausführen kann.
   Jede OS‑Domäne erhält eigene GPU‑Register, VRAM‑Bereiche und Command‑Queues.
   Dadurch können mehrere Betriebssysteme gleichzeitig Render‑ oder Compute‑Aufgaben
   ausführen, ohne sich gegenseitig zu blockieren.

3. **PCIe‑Multiplexing‑Layer + Firmware‑Abstraktions‑Layer (FAL)**  
   Eine neue Hardware‑/Firmware‑Schicht, die PCIe‑Geräte dynamisch und parallel
   mehreren Betriebssystemen zuweisen kann.  
   Der **Firmware‑Abstraktions‑Layer (FAL)** übernimmt PCIe‑Routing, DMA‑Isolation,
   Interrupt‑Trennung und Geräte‑Arbitration.  
   Diese Schicht ist zwingend notwendig, da klassisches BIOS/UEFI keine
   Multi‑Domain‑PCIe‑Hardware initialisieren oder verwalten kann.

4. **Dual‑OS‑Firmware‑Modell**  
   Eine Firmware, die zwei Betriebssysteme gleichzeitig booten und verwalten kann.
   Jede Domäne erhält eigene ACPI‑Tabellen, Interrupt‑Routen und Hardware‑Abstraktionen.
   Die Firmware initialisiert und kontrolliert beide OS‑Domänen parallel.

## Neue Boot‑Architektur (BIOS‑Ersatz)

Da NEXOD auf Hardware basiert, die in heutigen Systemen nicht existiert,
benötigt es ein **vollständig neues Boot‑Konzept**.

NEXOD ersetzt BIOS/UEFI vollständig und ist die erste Komponente, die nach dem Einschalten läuft:

1. Einschalten → NEXOD‑Firmware startet  
2. Hardware‑Domänen werden initialisiert  
3. CPU/GPU/PCIe‑Ressourcen werden partitioniert  
4. Speicher und Interrupts werden isoliert  
5. Mehrere Betriebssysteme werden parallel gestartet  

Dieses neue Boot‑Modell ist zwingend notwendig, da klassisches BIOS/UEFI
keine Multi‑Domain‑Hardware initialisieren oder verwalten kann.

## Vision

Durch diese Komponenten ermöglicht NEXOD eine völlig neue Form des Computings:
Windows, Linux oder andere Systeme können gleichzeitig nativ laufen – sichtbar auf
mehreren Displays oder per Tastenkombination sofort wechselbar. Entwickler können
Software parallel testen, Nutzer benötigen keine zwei Geräte mehr, und moderne
Hardware wird erstmals vollständig ausgenutzt.

---

# 🇷🇺 Русский Abstract

NEXOD (Next‑Gen Operating System Device) описывает новую архитектуру компьютера,
способную нативно и одновременно запускать несколько операционных систем на одном
и том же оборудовании. В отличие от виртуализации или dual‑boot, каждая ОС получает
собственный полностью изолированный аппаратный домен – без эмуляции, без
модифицированных драйверов и без потери производительности.

Чтобы обеспечить такой уровень нативного параллелизма, NEXOD вводит четыре новые аппаратные концепции:

1. **Dual‑Domain‑Execution CPU**  
   Процессор, способный одновременно выполнять два полностью разделённых домена.
   Каждый домен имеет собственные регистры, таблицы прерываний, таблицы страниц
   и уровни привилегий. Обе ОС работают параллельно и каждая считает, что находится
   в настоящем root‑режиме – без какого‑либо слоя виртуализации.

2. **Multi‑Context GPU**  
   Графический процессор, способный выполнять несколько реальных аппаратных
   контекстов одновременно. Каждый домен ОС получает собственные GPU‑регистры,
   области VRAM и очереди команд. Это позволяет нескольким ОС выполнять графические
   или вычислительные задачи параллельно, не блокируя друг друга.

3. **PCIe Multiplexing Layer + Firmware Abstraction Layer (FAL)**  
   Новый аппаратно‑прошивочный слой, который может динамически и параллельно
   распределять PCIe‑устройства между несколькими ОС.  
   **FAL** управляет PCIe‑маршрутизацией, изоляцией DMA, разделением прерываний
   и арбитражем устройств.  
   Этот слой необходим, потому что традиционный BIOS/UEFI не способен
   инициализировать или управлять многодоменной PCIe‑архитектурой.

4. **Dual‑OS Firmware Model**  
   Прошивка, способная одновременно загружать и управлять двумя операционными
   системами. Каждый домен получает собственные ACPI‑таблицы, маршрутизацию
   прерываний и аппаратные абстракции. Прошивка инициализирует и контролирует
   оба домена параллельно.

## Новая загрузочная архитектура (замена BIOS)

Поскольку NEXOD основан на аппаратуре, которой не существует в современных системах,
он требует **полностью новой загрузочной архитектуры**.

NEXOD полностью заменяет BIOS/UEFI и становится первым компонентом, который
запускается после подачи питания:

1. Включение питания → запускается прошивка NEXOD  
2. Инициализируются аппаратные домены  
3. CPU/GPU/PCIe‑ресурсы разделяются  
4. Память и прерывания изолируются  
5. Несколько ОС запускаются параллельно  

Эта новая модель загрузки необходима, потому что традиционный BIOS/UEFI
не способен инициализировать или управлять многодоменной аппаратурой.

## Видение

Благодаря этим компонентам NEXOD открывает совершенно новый подход к вычислениям:
Windows, Linux и другие системы могут работать нативно и одновременно – на разных
дисплеях или с мгновенным переключением по горячей клавише. Разработчики могут
тестировать ПО параллельно, пользователям не нужны два устройства, а современное
оборудование впервые используется полностью.
