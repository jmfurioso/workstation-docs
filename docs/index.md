<img src="assets/mono.jpg" width="160" align="right" alt="Mono">

# Mono's Workstation


Welcome to the **Mono's Workstation** operations portal.

This site contains everything required to build, configure, validate, and maintain a Linux workstation.

---

## 🚀 What would you like to do?

<div class="grid cards" markdown>

-   ### 🚀 Build a Workstation

    Commission a brand-new CachyOS workstation from scratch.

    <a href="workstation-rollout/" class="md-button md-button--primary">
    Start Rollout
    </a>

-   ### 🧰 Install Components

    Install workstation-specific applications.

    <a href="component-installers/" class="md-button md-button--primary">
    Component Installers
    </a>

-   ### 🎨 Personalization

    Desktop theme, Microsoft PWAs and optional customization.

    <a href="desktop-customization/" class="md-button md-button--primary">
    Personalization
    </a>

-   ### ✅ Validate

    Verify the workstation before placing it into service.

    <a href="acceptance-test/" class="md-button md-button--primary">
    Acceptance Test
    </a>

-   ### 💾 Disaster Recovery

    Backup strategy, recovery procedures and infrastructure planning.

    <a class="md-button">
    Coming Soon
    </a>

</div>

---

## 📊 Current Project Status

| Area | Status |
|:-----|:------:|
| Commissioning | ✅ Stable |
| Bootstrap | ✅ Stable |
| Component Installers | ✅ Stable |
| Desktop Personalization | 🟡 Manual |
| Disaster Recovery | 🚧 Planning |

---

## ⚡ Quick Commands

### Update

```bash
git pull --rebase
```

### Bootstrap

```bash
./scripts/bootstrap.sh
```

### Capture

```bash
./scripts/capture-workstation.sh
```
