# Graph Report - second-brain-writeup  (2026-09-29)

## Corpus Check
- 3 files · ~7,506 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 72 nodes · 70 edges · 7 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `660e3787`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Накопительный «второй мозг» поверх Claude Code
- An accumulative "second brain" on top of Claude Code
- Заложенные принципы
- Design principles
- 3. Продукты: что сделано, насколько работает, какая сложность
- Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации
- 2. Как мы росли: хронология

## God Nodes (most connected - your core abstractions)
1. `An accumulative "second brain" on top of Claude Code` - 16 edges
2. `Накопительный «второй мозг» поверх Claude Code` - 16 edges
3. `3. Продукты: что сделано, насколько работает, какая сложность` - 12 edges
4. `Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации` - 10 edges
5. `2. Как мы росли: хронология` - 7 edges
6. `Design principles` - 6 edges
7. `Заложенные принципы` - 6 edges
8. `In one paragraph` - 1 edges
9. `Scale (snapshot on 17.06.2026, numbers verified)` - 1 edges
10. `Architecture: four loops` - 1 edges

## Surprising Connections (you probably didn't know these)
- None detected - all connections are within the same source files.

## Communities (7 total, 0 thin omitted)

### Community 0 - "Накопительный «второй мозг» поверх Claude Code"
Cohesion: 0.12
Nodes (15): Архитектура: 4 контура, Время и объём работы, Главный вывод, Зрелость, Как это росло, Контур защиты: правила и хуки, Контур обучения: 8 фаз, Контур памяти: 6 уровней (+7 more)

### Community 1 - "An accumulative "second brain" on top of Claude Code"
Cohesion: 0.13
Nodes (15): An accumulative "second brain" on top of Claude Code, Architecture: four loops, Bottom line, Honest limitations, How it grew, In one paragraph, Learning loop: eight phases, Maturity (+7 more)

### Community 2 - "Заложенные принципы"
Cohesion: 0.33
Nodes (6): 1. Zettelkasten: атомарное связанное знание, 2. Граф знаний: направленная scale-free сеть, 3. Накопительная самоэволюция (подход Карпатти), 4. Межпроектность: общая память как несущая конструкция, 5. Версионируемое переносимое хранение, Заложенные принципы

### Community 3 - "Design principles"
Cohesion: 0.33
Nodes (6): 1. Zettelkasten: atomic linked knowledge, 2. Knowledge graph: a directed scale-free network, 3. Accumulative self-evolution (the Karpathy approach), 4. Cross-project memory as a load-bearing structure, 5. Versioned, portable storage, Design principles

### Community 4 - "3. Продукты: что сделано, насколько работает, какая сложность"
Cohesion: 0.17
Nodes (12): 3.10. Работа с медиа и знаниями — сложность 2/5, 3.11. Исследования и прототипы (честно — не продукты), 3.1. Платформа правил и судейства для спортивной федерации — сложность 5/5, 3.2. Школьное расписание и кабинет завуча — сложность 4/5, 3.3. CRM и аналитика соревнований для спортивной академии — сложность 5/5, 3.4. Автоматизация для горно-металлургического холдинга (под НДА) — сложность 5/5, 3.5. Сайт подбора автомобильных аккумуляторов — сложность 4/5, 3.6. Закрытый корпоративный мессенджер — сложность 4/5 (+4 more)

### Community 5 - "Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации"
Cohesion: 0.22
Nodes (8): 1. Кто мы и в чём подход, 4. Сводная карта продуктов, 5. Как устроена наша работа с ИИ (то, что отличает нас), 6. Пять поворотных моментов: ошибка → правило → результат, 7. Технологический стек, 8. Чем мы честно ограничены, 9. Что мы можем сделать для вас, Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации

### Community 6 - "2. Как мы росли: хронология"
Cohesion: 0.29
Nodes (7): 2. Как мы росли: хронология, Август — промышленная эксплуатация, Апрель — фундамент: сначала правила, потом код, Июль — выход на сложные предметные области, Июнь — упрочнение: честные метрики, Май — взросление: правило записано ≠ правило выполняется, Сентябрь — масштаб и дисциплина работы с заказчиком

## Knowledge Gaps
- **62 isolated node(s):** `In one paragraph`, `Scale (snapshot on 17.06.2026, numbers verified)`, `Architecture: four loops`, `1. Zettelkasten: atomic linked knowledge`, `2. Knowledge graph: a directed scale-free network` (+57 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `An accumulative "second brain" on top of Claude Code` connect `An accumulative "second brain" on top of Claude Code` to `Накопительный «второй мозг» поверх Claude Code`, `Design principles`?**
  _High betweenness centrality (0.256) - this node is a cross-community bridge._
- **Why does `Накопительный «второй мозг» поверх Claude Code` connect `Накопительный «второй мозг» поверх Claude Code` to `Заложенные принципы`?**
  _High betweenness centrality (0.256) - this node is a cross-community bridge._
- **Why does `Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации` connect `Инженерная практика с ИИ: полгода, 20+ продуктов, 6 систем в эксплуатации` to `3. Продукты: что сделано, насколько работает, какая сложность`, `2. Как мы росли: хронология`?**
  _High betweenness centrality (0.106) - this node is a cross-community bridge._
- **What connects `In one paragraph`, `Scale (snapshot on 17.06.2026, numbers verified)`, `Architecture: four loops` to the rest of the system?**
  _62 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Накопительный «второй мозг» поверх Claude Code` be split into smaller, more focused modules?**
  _Cohesion score 0.11764705882352941 - nodes in this community are weakly interconnected._
- **Should `An accumulative "second brain" on top of Claude Code` be split into smaller, more focused modules?**
  _Cohesion score 0.13333333333333333 - nodes in this community are weakly interconnected._