# Slashing module specification

## Abstract

This section specifies the slashing module of the Commercio.network based on Cosmos SDK

The slashing module enables Commercio.network blockchain to disincentivize any attributable action
by a protocol-recognized actor with value at stake by penalizing them ("slashing").

Penalties may include, but are not limited to:
- Burning some amount of their stake
- Removing their ability to vote on future blocks for a period of time.

This module will be used by the Commercio.network, a sovreign blockchain build on  the Cosmos ecosystem.

| Value | Description  | Status |
| --- | --- | --- |
| 1% | Slashing after 10.000 Blocks of inactivity  | `Jailing` |
| 5% | Slashing after Double signing  | `Tombstone` |


## Contents

1. **[Concepts](01_concepts.md)**
    - [States](01_concepts.md#states)
    - [Tombstone Caps](01_concepts.md#tombstone-caps)
    - [ASCII timelines](01_concepts.md#ascii-timelines)
2. **[State](02_state.md)**
    - [Signing Info](02_state.md#signing-info)
3. **[Messages](03_messages.md)**
    - [Unjail](03_messages.md#unjail)
4. **[Begin-Block](04_begin_block.md)**
    - [Evidence handling](04_begin_block.md#evidence-handling)
    - [Uptime tracking](04_begin_block.md#uptime-tracking)
5. **[05_hooks.md](05_hooks.md)**
    - [Hooks](05_hooks.md#hooks)
6. **[Tags](06_tags.md)**
    - [Handlers](06_tags.md#handlers)
7. **[Staking Tombstone](07_tombstone.md)**
    - [Abstract](07_tombstone.md#abstract)
