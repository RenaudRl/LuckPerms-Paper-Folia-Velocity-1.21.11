# LuckPerms-Folia (BTC Studio Fork)

![Java Version](https://img.shields.io/badge/Java-21-orange)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Target](https://img.shields.io/badge/Target-Paper%20/%20Folia-blue)

**LuckPerms-Folia** is a high-performance, streamlined fork of LuckPerms optimized specifically for **Paper/Folia 1.20+** and **Velocity 3.x**. 

This fork is maintained by **BTC Studio** and aims to provide the best possible permissions experience for modern Minecraft server environments by stripping away legacy platform support and integrating native Folia/Paper APIs.

---

## 🚀 Key Features

- **Native Folia Architecture**: Built from the ground up to support Folia's region-based multithreading.
  - Utilizes `RegionScheduler` and `AsyncScheduler` for thread-safe operations.
  - Performance-tuned database handling with **HikariCP 6.3.0**.
- **Advanced Contexts**:
  - `folia:region`: Define permissions based on the specific Folia region coordinates.
  - `folia:tps`: Granular performance-based permissions (5s, 15s, 1m, 5m, 15m averages).
- **MiniMessage Deep Integration**:
  - Full support for <gradient>, <rainbow>, and other modern tags in prefixes, suffixes, and messages.
  - Highly configurable conversion for legacy plugin compatibility.
- **Paper Optimization**:
  - Leverages `AsyncTabCompleteEvent` for non-blocking, lightning-fast command completions.
  - Full support for Paper's native `Audience` and `Component` APIs.

---

## ⚙️ Configuration

We've added new configuration keys to `config.yml` specifically for this fork:

| Key | Default | Description |
|-----|---------|-------------|
| `use-minimessage` | `true` | Enables MiniMessage parsing for all general plugin messages. |
| `use-minimessage-for-metadata` | `true` | If enabled, prefixes and suffixes will be parsed via MiniMessage before being sent to the client. |

---

## 🛠 Building

LuckPerms-Folia uses Gradle and requires **Java 21**.

```sh
# Clone the repository
git clone https://github.com/RenaudRl/LuckPerms-Paper-Folia-Velocity-1.21.11.git
cd LuckPerms-Paper-Folia-Velocity-1.21.11

# Build the project
./gradlew clean build -x test
```

### Artifact Locations:
- **Paper/Folia**: `bukkit/loader/build/libs/LuckPerms-Bukkit-5.5.24.jar`
- **Velocity**: `velocity/build/libs/LuckPerms-Velocity-5.5.24.jar`

---

## 🤝 Support & Contribution

Support for this fork is provided by **BTC Studio**. Please do not report issues encountered in this fork to the original LuckPerms project.

- **Maintained by**: [BTC Studio](https://github.com/RenaudRl)
- **Original Project**: [LuckPerms](https://github.com/LuckPerms/LuckPerms)

## 📜 License
Licensed under the **MIT License**.
