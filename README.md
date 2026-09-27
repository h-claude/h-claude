# Hi there, I'm Hippolyte 👋

```
Master's Student @ 42, specializing in Cybersecurity
📍 Paris, France
```

A software engineer with a systems programming background, now focused on cybersecurity: identity & access management (OAuth2, 2FA), network segmentation, TLS/SSL, and defensive C/C++ programming. I like building software where correctness and memory safety actually matter — shells, servers, and network architectures.

---

## 🚀 Featured Projects

### 🐚 [Minishell](https://github.com/h-claude/minishell)
> A POSIX-compliant command interpreter in C that lexes, parses into an AST, and executes pipelines of external and built-in commands with I/O redirection.

- **Problem & Classification:** Shell Implementation — lexing, recursive-descent parsing, and process orchestration.
- **Key Engineering:** AST-based parser flattened into pipelines, custom garbage collector for leak-free allocation tracking, context-aware signal handling (interactive prompt, heredoc, child processes), built-ins (`cd`, `echo`, `env`, `exit`, `export`, `pwd`, `unset`) implemented in-process.
- **Reliability:** `-Wall -Wextra -Werror`, deterministic cleanup via `fork`/`execve`/`waitpid`/`pipe`/`dup2`.
- **Security:** Rigorous manual memory management with zero leaks (Valgrind-verified) to eliminate memory corruption vectors, process isolation for every executed command.
- **Tech Stack:** `C (C99)`, `GNU Readline`, `Makefile`, `Linux`

---

### 🎯 [cub3D](https://github.com/h-claude/cub3d)
> A ray-casting engine parsing custom `.cub` scene files to render real-time, textured first-person 3D projections of 2D maps — inspired by Wolfenstein 3D's rendering technique.

- **Problem & Classification:** Real-time Graphics — ray marching, texture mapping, and map validation.
- **Key Engineering:** Per-column ray marching with distance-based depth shading, cardinal-direction texture lookup, recursive flood-fill map enclosure verification, mouse-look and FPS/CPU/RAM HUD (bonus).
- **Reliability:** Deterministic cleanup on every parsing error path, cross-platform memory sampling (Linux/macOS).
- **Tech Stack:** `C`, `MLX42 (GLFW)`, `Makefile / CMake`

---

### 🎮 [ft_transcendence](https://github.com/h-claude/ft_transcendence)
> A real-time multiplayer Pong platform combining an authoritative WebSocket game server, OAuth2/TOTP authentication, tournament orchestration, and blockchain-based score notarization.

- **Problem & Classification:** Full-stack Real-time Web App — authoritative game server, matchmaking, and GitOps-style deployment.
- **Key Engineering:** 60 Hz tick-rate physics server, JWT + httpOnly cookie auth with TOTP 2FA, FIFO matchmaking queue, tournament bracket state machine, on-chain score persistence on Avalanche Fuji testnet, AI opponent with trajectory prediction.
- **Reliability:** Session recovery with reconnection grace period, boot-time state sanitization, Nginx TLS reverse proxy.
- **Security:** End-to-end OAuth2 + TOTP 2FA, REST/WebSocket endpoints secured with JWTs, strict server-side validation (Zod) to prevent injection risks.
- **Tech Stack:** `Node.js 20`, `Fastify`, `TypeScript`, `SQLite`, `ethers.js`, `Docker Compose`, `Nginx` — plus a `C++20` terminal client (`FTXUI`, `IXWebSocket`)

---

### 🌐 [webserv](https://github.com/h-claude/webserv)
> A single-threaded, non-blocking HTTP/1.1 server in C++98 that uses `poll()` multiplexing to handle listening sockets, client connections, and CGI subprocess pipes simultaneously.

- **Problem & Classification:** Network I/O Multiplexing — Reactor pattern over a unified event loop.
- **Key Engineering:** Per-connection finite state machine (`WAITING_HEADERS → WAITING_BODY → PROCESSING → CGI_WRITING → CGI_READING → RESPONDING`), virtual hosting via Host header, CGI execution through forked pipes, keep-alive, multipart file uploads, hand-written config parser.
- **Reliability:** Graceful shutdown on `SIGINT`/`SIGQUIT`, leak-free under Valgrind.
- **Tech Stack:** `C++98`, `poll()`, `POSIX Sockets`, `Makefile`

---

### 📡 [IoT (Inception of Things)](https://github.com/h-claude/ft_Inception-of-Things)
> A three-stage Kubernetes infrastructure progression: a two-node K3s cluster via Vagrant, a single-node setup with virtual-hosted apps behind Traefik Ingress, and a K3d cluster running Argo CD for GitOps continuous deployment.

- **Problem & Classification:** Container Orchestration & GitOps — cluster bootstrap, ingress routing, and continuous deployment.
- **Key Engineering:** Deterministic multi-node cluster bootstrap via shared token exchange, host-name-based HTTP routing to independently-scaled backends, Argo CD reconciliation loop for GitOps automation, cross-architecture support via QEMU emulation.
- **Tech Stack:** `K3s`, `K3d`, `Vagrant / VirtualBox`, `Traefik Ingress`, `Argo CD`, `Docker CE`

---

## 🛠️ Technical Arsenal

| Domain | Technologies & Tooling |
| :--- | :--- |
| **Languages** | C, C++ (98/20), Python, TypeScript, JavaScript, SQL, Assembly (x86-64), Shell |
| **Security & Systems** | OAuth2, 2FA/TOTP, TLS/SSL, Network Segmentation, Defensive C/C++, Memory Safety, Unix Internals |
| **Systems & Networking** | POSIX Sockets, `poll()`/multiplexing, Signals, IPC (pipes, fork/exec) |
| **Backend & Web** | Node.js, Fastify, WebSockets, SQLite, JWT |
| **DevOps & Infrastructure** | Docker, Docker Compose, Kubernetes (K3s/K3d), Vagrant, Argo CD, Nginx |
| **Profiling & Diagnostics** | GDB, Valgrind, Clang Sanitizers |

---

## 📬 Let's Connect

- **Email:** [hippolyteclaude@icloud.com](mailto:hippolyteclaude@icloud.com)
