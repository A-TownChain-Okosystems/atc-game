# Component Plan — atc-game

This document details the components, primary data structures, and core functions implemented in `atc-game`.

## Core Component Specification

### 1. Battle System (`battle/battle_system.atc`)
- **Module**: `battle_system`
- **ATC Standard**: `ATC-90`
- **Description**: Turn-based, stats, damage, abilities, loot
- **Key Data Structure**: `BattleState`
- **Key Function**: `execute_turn()` — Calculates combat damage, ability effects, and updates battle state

### 1. Character Engine (`character/character_engine.atc`)
- **Module**: `character_engine`
- **ATC Standard**: `ATC-90`
- **Description**: Bio, stats, progression, inventory
- **Key Data Structure**: `CharacterProfile`
- **Key Function**: `level_up()` — Increases character level and calculates stat progression bonuses

### 1. Anti-Cheat (`security/anticheat.atc`)
- **Module**: `anticheat`
- **ATC Standard**: `ATC-90`
- **Description**: Move validation, replay detection, stat checks
- **Key Data Structure**: `CheatCheck`
- **Key Function**: `validate_movement()` — Validates player movement delta against maximum allowed physical bounds

### 1. Timeline Engine (`timeline/timeline_engine.atc`)
- **Module**: `timeline_engine`
- **ATC Standard**: `ATC-90`
- **Description**: Events, triggers, story progression
- **Key Data Structure**: `TimelineEvent`
- **Key Function**: `trigger_event()` — Executes story or gameplay event when game tick reaches target

### 1. Quest System (`quests/quest_system.atc`)
- **Module**: `quest_system`
- **ATC Standard**: `ATC-90`
- **Description**: Quest generation, tracking, rewards
- **Key Data Structure**: `QuestState`
- **Key Function**: `complete_quest()` — Verifies quest objective completion and grants player rewards

### 1. Game Physics (`physics/game_physics.atc`)
- **Module**: `game_physics`
- **ATC Standard**: `ATC-90`
- **Description**: Collision, gravity, movement, zones
- **Key Data Structure**: `PhysicsBody`
- **Key Function**: `detect_collision()` — Checks bounding box intersections between active physics entities

