# UIN-Campus

Système de gestion académique de l'UIN (projet fil rouge du cours de POO en C++ moderne).

## Versions des outils

| Outil | Version |
|---|---|
| g++ | 15.2.0 |
| clang++ | 21.1.8 |
| cmake | 4.2.3 |
| ninja | 1.13.2 |
| gdb | 17.1 |
| git | 2.53.0 |

Environnement : WSL2 (Ubuntu) sous Windows, VS Code avec clangd.

## Construction

```bash
cmake --preset debug
cmake --build --preset debug
./build/debug/uin-campus
```

Version release :

```bash
cmake --preset release
cmake --build --preset release
./build/release/uin-campus
```

Résultat attendu :

```
UIN-Campus — Système de gestion académique
Version 0.1.0
```

## Qualité du code

```bash
clang-format -i include/uincampus/*.hpp src/*.cpp app/*.cpp
clang-tidy -p build/debug src/*.cpp app/*.cpp
```