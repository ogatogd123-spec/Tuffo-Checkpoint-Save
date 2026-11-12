# Tuffo Checkpoints Save

Projeto inicial Geode para Geometry Dash 2.2081 — Android 64-bit.

## Estado atual

Este ZIP é um **esqueleto de desenvolvimento**, não um mod final.
Ele contém o manifesto, CMake e ponto de entrada C++ para iniciar a
compilação Android. **Ainda não salva nem restaura checkpoints.**

A lógica de checkpoint depende de serializar/restaurar corretamente o
estado do jogo (PlayLayer, player, checkpoints, timers, objetos e estado
dos triggers). Não é seguro fingir que apenas gravar a posição do jogador
produz um save válido.

## Requisitos

- Geometry Dash 2.2081
- Geode SDK compatível com GD 2.2081 (Geode 5.x)
- Android NDK suportado pelo SDK
- Dependências declaradas em `mod.json`:
  - `geode.node-ids`
  - `sabe.persistenceapi`

## Próxima etapa técnica

Portar a implementação GPL do PlatformerSaves 2.2081, conferir todos os
hooks e bindings em Android64 e compilar um `.geode` Android64 real.
O repositório de referência declara suporte a Android e requer Geode 5.6.1+
e PersistenceAPI 1.1.0.

Referência:
https://github.com/BANANCHIKIREAL/PlatformerSaves

## Estrutura

```text
Tuffo-Checkpoints-Save/
├── .github/workflows/android.yml
├── src/main.cpp
├── CMakeLists.txt
├── mod.json
└── README.md
```

## Identidade

- Nome: Tuffo Checkpoints Save
- ID: `tuffo.checkpointssave`
- Versão inicial: `0.1.0`
- Plataforma alvo: `android64`
