# com.kruty1918.entity-health

Reusable entity-health primitives extracted from Moyva: `IHealth` (hp/destroyed/events
contract), `HealthComponent` (MonoBehaviour impl), `IHealthRegistry`/`HealthRegistry`
(entityId keyed lookup). Damage formulas, death/capture rules and network
authority stay host-side.

## Install (Unity Package Manager)

Package Manager → **+** → **Add package from git URL**:

```
https://github.com/kruty1918dev-ai/com.kruty1918.entity-health.git
```

or in `Packages/manifest.json`:

```json
"com.kruty1918.entity-health": "https://github.com/kruty1918dev-ai/com.kruty1918.entity-health.git#v0.1.0"
```

The repository is private — Git credentials (PAT / Git Credential Manager)
are required on every machine that resolves the package.

## API surface

| Type | Purpose |
|---|---|
| `IHealth` | Hit-points contract: current/max, damaged/healed/destroyed events |
| `HealthComponent` | `IHealth` MonoBehaviour implementation for scene entities |
| `IHealthRegistry` / `HealthRegistry` | Keyed `entityId → IHealth` lookup |

## Model

The package deliberately stops at primitives: damage formulas, death/capture
rules and network authority are host-game concerns.
