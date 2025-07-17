# 🦀 Rust 100% Repository

Want GitHub to **show Rust as the main language** in your repository instead of Makefiles or TOML? Here's how to set it up correctly.

---

## 🗂 Required Files

Add these to the **root** of your repository:

```
.gitattributes
.gitignore
```

---

## 📁 `.gitattributes`

```gitattributes
**/target/** linguist-vendored
Makefile linguist-detectable=false
Cargo.lock linguist-detectable=false
*.toml linguist-detectable=false
*.rs linguist-language=Rust
```

This tells GitHub Linguist:

- Ignore compiled code (`target/`)
- Don’t count `Makefile`, `Cargo.lock`, or `.toml` files
- Force all `.rs` files to be recognized as **Rust**

---

## 📁 `.gitignore` (Optional but Recommended)

```gitignore
**/target
```

This avoids committing compiled files.

---

## ✅ Done!

Commit and push, and GitHub will now **show Rust as your main language** 🦀

---

## 📜 License

MIT — Free to use, modify, and share.  
Happy coding in Rust! 🚀🔥
