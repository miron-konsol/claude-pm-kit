# Скиллы Claude Code для продактов и маркетологов

Набор скиллов, которые превращают одну команду `/имя` в проверенный фреймворк — для продуктовой стратегии, идей и упаковки. Плюс воркшоп «Как я работаю с Клодом».

🔗 **Живой сайт:** https://claude-workshop-iota.vercel.app

> **Что такое скилл?** Это готовый навык Клода: папка с файлом `SKILL.md`. Клод подхватывает его по команде `/имя-скилла` и ведёт по шагам. Вместо длинного промпта — одно слово.

---

## 📦 6 скиллов

| Скилл | Что делает | Пример запроса |
|---|---|---|
| `/product-strategy` | Полная продуктовая стратегия (рынок → роадмап) в интерактивный HTML | «Построй продуктовую стратегию для нашего LMS на рынке РФ, горизонт 12 месяцев» |
| `/product-marketing` | Единый контекст-документ о продукте, ICP и позиционировании | «Настрой контекст продукта: ICP, позиционирование, боли — черновик из репозитория» |
| `/blue-ocean-strategy` | Уход из ценовых войн в голубой океан (ERRC, Strategy Canvas) | «Найди голубой океан для нашего SaaS — прогони через ERRC и strategy canvas» |
| `/brainstorming` | Превращает идею в согласованную спеку до кода | «Хочу добавить push-реактивацию. Давай разберём, что именно строим» |
| `/marketing-ideas` | 139 идей роста под твой этап, бюджет и команду | «B2B SaaS, early stage, бюджет ноль, команда 3 — дай маркетинговые идеи» |
| `/marketing-psychology` | Когнитивные искажения для роста конверсии | «Юзеры бросают оплату на pricing — какие психологические модели применить?» |

---

## 🔌 Как подключить

Скиллы из трёх источников — единой команды нет.

### 1. `brainstorming` — плагин superpowers
```
/plugin marketplace add anthropics/claude-plugins-official
/plugin install superpowers@claude-plugins-official
```
Исходник: https://github.com/obra/superpowers

### 2. `blue-ocean-strategy` — marketplace wondelai
```
/plugin marketplace add wondelai/skills
/plugin install strategy-growth@wondelai-skills
```
Исходник: https://github.com/wondelai/skills

### 3. `product-strategy`, `product-marketing`, `marketing-ideas`, `marketing-psychology` — личные скиллы
Лежат в этом репозитории в папке [`skills/`](./skills). Чтобы поставить — скопируй нужную папку к себе:
```bash
# пример для одного скилла
mkdir -p ~/.claude/skills
cp -r skills/product-strategy ~/.claude/skills/
```
Или забери весь набор:
```bash
git clone https://github.com/miron-konsol/claude-pm-kit
cp -r claude-pm-kit/skills/* ~/.claude/skills/
```

**Проверить:** набери `/` в Claude Code — скилл появится в списке.

---

## 🧭 Как применять — цепочкой

**Продакт:** `/product-marketing` (зафиксировать контекст) → `/product-strategy` (собрать стратегию) → `/blue-ocean-strategy` (проверить позиционирование) → `/brainstorming` (каждую фичу до кода).

**Маркетолог:** `/product-marketing` (тот же контекст-файл) → `/marketing-ideas` (выбрать каналы) → `/marketing-psychology` (усилить конверсию) → профильные скиллы (ads, copywriting, cro).

---

## 📄 Лицензии / источники
- `brainstorming` — из проекта [superpowers](https://github.com/obra/superpowers).
- `blue-ocean-strategy` — из [wondelai/skills](https://github.com/wondelai/skills), по книге W. Chan Kim & R. Mauborgne «Blue Ocean Strategy».
- `product-strategy` — авторский скилл.
- `product-marketing`, `marketing-ideas`, `marketing-psychology` — маркетинг-пак (v2.0.0). Если ты автор набора и хочешь указать лицензию/атрибуцию — открой issue.

*Сайт и материалы собраны в Claude Code.*
