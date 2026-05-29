# moonchip

System configuration and specs repository for the moonChip computer.

## What's Here

- **SYSTEM_SPECS.md** — Hardware inventory and performance profile
- **configs/** — System configuration files (dotfiles, settings, etc.)
- **backups/** — Backup of important system data

## Purpose

Track and version control critical system settings, configurations, and hardware specs so you can:
- Keep a history of system changes
- Restore configs after a fresh install
- Remote access and manage this computer's setup
- Document hardware for troubleshooting

## Getting Started

Add system config files here as needed:
```bash
cp ~/.bashrc configs/
cp ~/.config/firefox/ configs/firefox-profile/
```

Then commit:
```bash
git add configs/
git commit -m "Add system configurations"
```
