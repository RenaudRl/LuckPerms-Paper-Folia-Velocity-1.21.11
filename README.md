# LuckPerms-Folia

![Java Version](https://img.shields.io/badge/Java-21-orange)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Target](https://img.shields.io/badge/Target-Paper%20/%20Folia%20/%20Velocity%20/%20BTC--CORE-blue)

**LuckPerms-Folia** is a high-performance, streamlined fork of **LuckPerms**, engineered specifically for **BTC Studio** infrastructure and the **BTC-CORE** server fork. It represents a modern approach to permission management, specifically optimized for **BTC-CORE (Paper/Folia 1.21.11+)** and **Velocity 3.x** by removing legacy baggage and focusing on native multi-threaded performance.

> [!WARNING]
> **DEVELOPER COMPATIBILITY NOTICE**
> LuckPerms-Folia introduces architectural changes to leverage Folia's regionized multithreading. Standard LuckPerms extensions or plugins that rely on synchronous API access may require auditing. This fork is tailored for environments where performance and Folia-native support are the highest priority.

---

## 🚀 Key Features in Detail

### ⚡ Concurrency & Architecture (Folia Integration)
- **Native Folia Support**: Fully integrated with Folia's `RegionScheduler` and `AsyncScheduler`, ensuring thread-safe permission checks and data handling.
- **Regionized Logic**: Permission contexts aware of Folia regions, allowing for granular control in multi-threaded environments.
- **BTC-CORE / ASPaper Optimization**: Native compatibility with BTC-CORE's high-performance architecture, ensuring zero impact on the fork's optimized tick loops and async systems.
- **HikariCP 6.3.0**: Upgraded connection pooling for ultra-fast, non-blocking database operations.

### 🎨 Modern Formatting (MiniMessage)
- **Deep MiniMessage Integration**: Full support for `<gradient>`, `<rainbow>`, and other modern tags in prefixes, suffixes, and plugin messages.
- **Legacy Compatibility**: Intelligent conversion layer to maintain compatibility with legacy formatting while favoring modern standards.
- **Metadata Parsing**: Metadata (prefixes/suffixes) can be configured to parse MiniMessage tags natively.

### 🛠️ Performance & Optimizations
- **Async Tab Completion**: Leverages Paper's `AsyncTabCompleteEvent` for non-blocking, lightning-fast command suggestions.
- **Native Paper APIs**: Extensive use of Paper's `Audience` and `Component` APIs to reduce overhead and improve compatibility.
- **Stripped Legacy**: Removed support for older Minecraft versions (pre-1.20) and non-Paper platforms to minimize the footprint and maximize speed.

---

## ⚙️ Configuration

LuckPerms-Folia introduces specific tuning options in `config.yml`.

### High-Priority Settings
| Key | Default | Description |
|-----|---------|-------------|
| `use-minimessage` | `true` | Enables MiniMessage parsing for all general plugin messages. |
| `use-minimessage-for-metadata` | `true` | Parses prefixes and suffixes via MiniMessage before sending to clients. |
| `folia-context-enabled` | `true` | Enables `folia:region` and `folia:tps` contexts. |

---

## 🛠 Building & Deployment

Requires **Java 21** and a strong understanding of Gradle.

```bash
# Clone the repository
git clone https://github.com/RenaudRl/LuckPerms-Paper-Folia-Velocity-1.21.11.git
cd LuckPerms-Paper-Folia-Velocity-1.21.11

# Build the project (skipping tests for faster cycles)
./gradlew clean build -x test
```

### Artifact Locations:
- **Paper/Folia**: `bukkit/loader/build/libs/LuckPerms-Bukkit-5.5.24.jar`
- **Velocity**: `velocity/build/libs/LuckPerms-Velocity-5.5.24.jar`

---

## 🤝 Credits & Inspiration
This project is built upon the innovation of the broader Minecraft development community:
- **[LuckPerms](https://github.com/LuckPerms/LuckPerms)** - The original, industry-standard permission plugin.
- **[BTC Studio](https://github.com/RenaudRl)** - Maintenance and specialized optimizations.

---

## 📜 License
Licensed under the **MIT License**. Original licenses apply to upstream components.

