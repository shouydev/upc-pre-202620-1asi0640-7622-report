    Nivel 1: FLSM Internacional (172.17.0.0/16)
    │   ├── Subred Argentina
    │   ├── Subred Chile
    │   ├── Subred Perú  ───────────────────────────────────────────┐
    │   ├── Subred Ecuador                                          │
    │   └── Subred Colombia                                         │
    │                                                               │
    Nivel 2: FLSM Nacional (Se reparte la subred de Perú) <─────────┘
    │   ├── Subred 1: Sede Lima  ─────────────────────────┐
    │   ├── Subred 2: Enlaces WAN (Se divide en /30) ─────┼─────────┐
    │   ├── Subred 3: Sede La Libertad ───────────────────┼──┐      │
    │   ├── Subred 4: Sede Ica ───────────────────────────┼──┼──┐   │
    │   ├── Subred 5: Sede Huánuco                        │  │  │   │
    │   └── Subred 6: Sede Puno                           │  │  │   │
    │                                                     │  │  │   │
    Nivel 3: VLSM Interno (Dentro de cada sede) <─────────┘  │  │   │
        ├── Dentro de Lima (VLSM):                           │  │   │
        │   ├── VLAN Ventas (123 hosts)        -> Máscara /25│  │   │
        │   ├── VLAN Administración (100 hosts)-> Máscara /25│  │   │
        │   ├── VLAN Marketing (37 hosts)      -> Máscara /26│  │   │
        │   ├── VLAN Servidores (15 hosts)     -> Máscara /28│  │   │
        │   └── ...                                          │  │   │
        ├── Dentro de La Libertad (VLSM) <───────────────────┘  │   │
        │   └── Sus propios departamentos y usuarios            │   │
        ├── Dentro de Ica (VLSM) <──────────────────────────────┘   │
        │   └── Sus propios departamentos y usuarios                │
        └── Dentro de los Enlaces WAN (VLSM de /30) <───────────────┘
            ├── WAN 1 (Lima - La Libertad) -> /30 (2 hosts)
            ├── WAN 2 (Lima - Ica)         -> /30 (2 hosts)
            └── ...