# lua2go ☕

> Your Lua, to‑go.  
> Fully embeddable **PureGo** bindings for the official Lua runtime — fast, portable, and CGO‑free.

---

## ✨ Features
- 🧩 **PureGo implementation** – build static binaries, no CGO toolchain.  
- ⚙️ **Official Lua runtime** – full 5.4/5.3 compatibility.  
- 🔒 **Sandbox‑ready** – configurable capability levels (safe, http, storage…).  
- 🚀 **Lightweight and fast** – ideal for plugins, extensions, or scripting hooks.  
- ☁️ **Cross‑platform** – macOS, Linux, Windows supported.

---

## 📦 Installation
```bash
go get github.com/statuzlabs/lua2go
```

---

## 🧠 Quick Start
```go
package main

import (
	"fmt"
	"github.com/statuzlabs/lua2go"
)

func main() {
	L := lua2go.New()
	defer L.Close()

	L.DoString(`print("☕ Lua2Go says hi!"); return 42`)
	val := L.PopInt()
	fmt.Println("Lua returned:", val)
}
```

**Output**
```
☕ Lua2Go says hi!
Lua returned: 42
```

---

## 🪄 API Overview
| Category | Purpose |
|-----------|----------|
| `runtime` | Basic state creation, stack ops, error handling |
| `modules` | Register / disable standard libraries |
| `sandbox` | Timeouts, capability levels |
| `interop` | Go <-> Lua type conversion helpers |

---

## ⚙️ Roadmap
- [ ] Minimal binding layer (`luaL_dostring`, basics)  
- [ ] Safe sandbox helpers  
- [ ] Capability system for Statuz integration  
- [ ] Module registration API  
- [ ] LuaJIT support (future)  
- [ ] Community extensions & benchmarks  

---

## 🧩 Example Use Cases
- Embed scripting in Go services (e.g. alert hooks in **Statuz**)  
- Automate workflows via user‑defined Lua functions  
- Rapid test or data‑transform scripting inside Go apps  

---

## 🤝 Contributing
Pull requests are welcome!  
Pending a CONTRIBUTING.md, feel free to open an issue with any ideas or feedback.

---

## 🧾 License
MIT © StatuzLabs  
> “Open source. Served fresh.”

---

## ☕ About StatuzLabs
We build tools that make uptime and transparency easy — from **Statuz** (the status‑page platform) to **lua2go** and beyond.  
Follow along at [github.com/statuzlabs](https://github.com/statuzlabs) for more open projects.
