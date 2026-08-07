# Hi, I'm Dmitry Karpenko 👋

### C# / .NET Backend & Systems Engineer

I build backend, networking and infrastructure-oriented applications with a focus on **reliability, data processing, concurrency and performance**.

My background combines software development with systems and network engineering, so I am especially interested in software that operates close to infrastructure: network telemetry, log processing, asynchronous pipelines, Linux services and production automation.

---

## 🚀 Featured Projects

### 📡 NetFlowv9

High-performance **NetFlow v9 collector** built with .NET 9.

The system receives traffic metadata from MikroTik routers over UDP, parses template-based flow records, processes them through bounded asynchronous pipelines and persists historical data in ClickHouse.

**Key technologies and concepts:**

* .NET 9 / C#
* UDP networking
* NetFlow v9
* `System.Threading.Channels`
* `ReadOnlySpan<byte>`
* `ArrayPool<byte>`
* bounded processing pipelines
* ClickHouse
* WebSockets
* Grafana
* Docker Compose

The project is used in a real internal network with MikroTik routers.

➡️ [NetFlowv9](https://github.com/KarpenkoDima/NetFlowv9)

---

### 📊 LogCollector

A lightweight **Syslog ingestion and processing service** for MikroTik devices.

The collector receives BSD Syslog messages over UDP, parses them without regular expressions or unnecessary intermediate strings, queues them through a bounded channel and writes batches to SQLite.

Loki and Grafana can be enabled for centralized log analysis.

**Key technologies and concepts:**

* .NET 9
* BSD Syslog / RFC 3164
* UDP
* `MemoryPool<byte>`
* zero-copy parsing
* bounded `Channel<T>`
* batching
* Dapper
* SQLite / WAL
* Loki
* Grafana
* Docker
* integration and end-to-end testing

➡️ [LogCollector](https://github.com/KarpenkoDima/LogCollector)

---

### 🏥 MedCert

A production Windows desktop application for generating and printing medical certificates.

The application was created for a real healthcare workflow and has been used in production for more than four years.

It automates document generation, printing confirmation, certificate history and repeat printing while operating completely offline on a single workstation.

**Key technologies and concepts:**

* C#
* .NET Framework 4.8
* Windows Forms
* LiteDB
* Microsoft Word / DOCX integration
* Dependency Injection
* Repository / Unit of Work
* NUnit
* Moq
* production legacy refactoring

The project demonstrates long-term maintenance and incremental modernization of real production software.

➡️ [MedCert](https://github.com/KarpenkoDima/MedCert)

---

## 🧪 Engineering Labs & Learning Projects

I also maintain smaller repositories used to study implementation details rather than only framework APIs.

### Networking & Systems

* [TCP-Book](https://github.com/KarpenkoDima/TCP-Book) — TCP and network programming experiments and educational implementations.
* [NetDissector](https://github.com/KarpenkoDima/NetDissector) — packet parsing experiments using `ReadOnlySpan<byte>`.
* [Distributed-FTP-Server](https://github.com/KarpenkoDima/Distributed-FTP-Server) — educational distributed-systems and FTP infrastructure lab.

### .NET Internals

* [CoreLinq](https://github.com/KarpenkoDima/CoreLinq) — learning how LINQ operators and iterators work internally.
* [asyncexpert-course](https://github.com/KarpenkoDima/asyncexpert-course) — async/await and concurrency exercises.
* [BatchWriterService](https://github.com/KarpenkoDima/BatchWriterService) — batching and asynchronous processing experiments.

### Data Access

* [EFCode-Advanced_Guide](https://github.com/KarpenkoDima/EFCode-Advanced_Guide) — EF Core experiments and advanced data-access notes.

---

## 🛠 Technologies

**Backend**

C# • .NET • ASP.NET Core • REST APIs • EF Core • Dapper

**Concurrency & Performance**

async/await • `Task` / `ValueTask` • `Channel<T>` • `Span<T>` • `Memory<T>` • memory pooling • batching • backpressure

**Networking**

TCP/IP • UDP • Syslog • NetFlow v9 • packet parsing • MikroTik

**Data**

SQL Server • SQLite • LiteDB • ClickHouse • Redis

**Infrastructure**

Linux • Docker • Docker Compose • Grafana • Loki • GitHub Actions

**Testing**

xUnit • NUnit • Moq • integration testing • end-to-end testing

---

## 🧠 Areas I Study

I am particularly interested in understanding what happens below high-level APIs:

* .NET async/await internals
* memory allocation and pooling
* high-throughput processing pipelines
* TCP/IP and network protocols
* Linux networking
* database query performance
* distributed systems
* observability and production diagnostics

---

## 📈 Current Focus

Currently developing and improving projects around:

**ASP.NET Core • high-performance .NET • networking • distributed systems • Linux infrastructure**

---

> I prefer projects where architecture and performance decisions can be explained in terms of actual data flow, resource ownership, failure modes and operational constraints.
