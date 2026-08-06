# Graph Report - second-brain-writeup  (2026-08-06)

## Corpus Check
- 3 files · ~4,933 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 48 nodes · 45 edges · 5 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `4ad2f2ee`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]

## God Nodes (most connected - your core abstractions)
1. `An accumulative "second brain" on top of Claude Code` - 16 edges
2. `Накопительный «второй мозг» поверх Claude Code` - 16 edges
3. `Design principles` - 6 edges
4. `Заложенные принципы` - 6 edges
5. `second-brain-writeup` - 3 edges
6. `§1 Состояние` - 1 edges
7. `§8 Open questions` - 1 edges
8. `In one paragraph` - 1 edges
9. `Scale (snapshot on 17.06.2026, numbers verified)` - 1 edges
10. `Architecture: four loops` - 1 edges

## Surprising Connections (you probably didn't know these)
- None detected - all connections are within the same source files.

## Import Cycles
- None detected.

## Communities (5 total, 0 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.12
Nodes (15): Архитектура: 4 контура, Время и объём работы, Главный вывод, Зрелость, Как это росло, Контур защиты: правила и хуки, Контур обучения: 8 фаз, Контур памяти: 6 уровней (+7 more)

### Community 1 - "Community 1"
Cohesion: 0.12
Nodes (15): An accumulative "second brain" on top of Claude Code, Architecture: four loops, Bottom line, Honest limitations, How it grew, In one paragraph, Learning loop: eight phases, Maturity (+7 more)

### Community 2 - "Community 2"
Cohesion: 0.33
Nodes (6): 1. Zettelkasten: атомарное связанное знание, 2. Граф знаний: направленная scale-free сеть, 3. Накопительная самоэволюция (подход Карпатти), 4. Межпроектность: общая память как несущая конструкция, 5. Версионируемое переносимое хранение, Заложенные принципы

### Community 3 - "Community 3"
Cohesion: 0.33
Nodes (6): 1. Zettelkasten: atomic linked knowledge, 2. Knowledge graph: a directed scale-free network, 3. Accumulative self-evolution (the Karpathy approach), 4. Cross-project memory as a load-bearing structure, 5. Versioned, portable storage, Design principles

### Community 4 - "Community 4"
Cohesion: 0.50
Nodes (3): §1 Состояние, §8 Open questions, second-brain-writeup

## Knowledge Gaps
- **40 isolated node(s):** `§1 Состояние`, `§8 Open questions`, `In one paragraph`, `Scale (snapshot on 17.06.2026, numbers verified)`, `Architecture: four loops` (+35 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `An accumulative "second brain" on top of Claude Code` connect `Community 1` to `Community 3`?**
  _High betweenness centrality (0.180) - this node is a cross-community bridge._
- **Why does `Накопительный «второй мозг» поверх Claude Code` connect `Community 0` to `Community 2`?**
  _High betweenness centrality (0.180) - this node is a cross-community bridge._
- **Why does `Design principles` connect `Community 3` to `Community 1`?**
  _High betweenness centrality (0.083) - this node is a cross-community bridge._
- **What connects `§1 Состояние`, `§8 Open questions`, `In one paragraph` to the rest of the system?**
  _40 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.125 - nodes in this community are weakly interconnected._
- **Should `Community 1` be split into smaller, more focused modules?**
  _Cohesion score 0.125 - nodes in this community are weakly interconnected._