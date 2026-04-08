# byDebut — Narrative Engine (Public Domain Ready)

---

## 🧠 Overview

byDebut is an identity-driven narrative engine that models stories as systems.

Instead of rewriting books, the platform:

* abstracts narrative structure
* exposes key variables
* simulates alternative outcomes
* generates original narratives

This ensures:

* legal safety (no copyrighted text reuse)
* infinite scalability
* user-driven story evolution

---

## ⚖️ Legal Foundation

The system is built on:

* Public domain works (e.g. Project Gutenberg)
* Original user-generated content
* Narrative abstraction (NOT text reproduction)

### Rules:

* ❌ No direct text reuse
* ❌ No Kindle/DRM sources
* ✅ Only abstracted narrative structures
* ✅ All generated output is original

---

## 📦 Repository Structure

```
/bydebut
  /data
    works.json
    characters.json
    variables.json
    decision_graphs.json
  /engine
    narrative_engine.ts
    constraint_engine.ts
    variation_generator.ts
  /api
    create_variation.ts
    get_work.ts
  /ui
    explore.tsx
    variation_view.tsx
  /legal
    terms.md
    content_policy.md
  README.md
```

---

## 🧩 Narrative Engine Schema

### Core Structure

```json
{
  "workId": "hamlet_shakespeare",
  "title": "Hamlet",
  "author": "William Shakespeare",
  "sourceType": "public_domain",
  "genre": ["tragedy"],
  "themes": ["revenge", "doubt", "identity"],
  "premise": "A prince confronts grief, betrayal, and the burden of action.",
  "worldModel": {},
  "characters": [],
  "narrativeVariables": [],
  "decisionGraph": {},
  "constraints": {},
  "variationTemplates": [],
  "comparisonFramework": {},
  "safetyRules": {},
  "provenance": {}
}
```

---

## 🌍 World Model

```json
{
  "worldModel": {
    "setting": {
      "timePeriod": "medieval",
      "location": "Denmark"
    },
    "worldRules": [
      "Royal authority defines justice",
      "Revenge is morally ambiguous"
    ],
    "tone": ["dark", "psychological"],
    "stakes": ["power", "truth", "revenge"]
  }
}
```

---

## 👤 Character Model

```json
{
  "characters": [
    {
      "characterId": "hamlet",
      "role": "protagonist",
      "archetype": "philosophical_prince",
      "coreDrives": ["truth", "justice"],
      "fears": ["uncertainty"],
      "initialState": {
        "mentalState": "conflicted"
      },
      "changeCapacity": "high"
    }
  ]
}
```

---

## 🎛️ Narrative Variables

```json
{
  "narrativeVariables": [
    {
      "variableId": "hesitation_level",
      "type": "scale",
      "min": 1,
      "max": 10,
      "defaultValue": 10,
      "impactScope": ["plot", "ending"]
    },
    {
      "variableId": "ghost_reliability",
      "type": "enum",
      "allowedValues": ["low", "medium", "high"],
      "defaultValue": "medium"
    }
  ]
}
```

---

## 🔗 Decision Graph

```json
{
  "decisionGraph": {
    "nodes": [
      { "nodeId": "ghost_event", "type": "event" },
      { "nodeId": "decision_point", "type": "decision" },
      { "nodeId": "conflict", "type": "event" },
      { "nodeId": "resolution", "type": "ending" }
    ],
    "edges": [
      { "from": "ghost_event", "to": "decision_point" },
      { "from": "decision_point", "to": "conflict" },
      { "from": "conflict", "to": "resolution" }
    ]
  }
}
```

---

## ⚙️ Constraint Engine

```json
{
  "constraints": {
    "hardConstraints": [
      "No copyrighted text reuse",
      "Maintain causal coherence"
    ],
    "softConstraints": [
      "Preserve emotional consistency"
    ]
  }
}
```

---

## 🧪 Variation Templates

```json
{
  "variationTemplates": [
    {
      "templateId": "single_change",
      "prompt": "Generate a new narrative where {{variable}} changes."
    },
    {
      "templateId": "moral_inversion",
      "prompt": "Invert the moral alignment of the protagonist."
    }
  ]
}
```

---

## 🔍 Comparison Framework

```json
{
  "comparisonFramework": {
    "dimensions": [
      "premise",
      "character_arc",
      "ending"
    ]
  }
}
```

---

## 🛡️ Safety Rules

```json
{
  "safetyRules": {
    "noTextReuse": true,
    "transformativeOnly": true
  }
}
```

---

## 📚 Sample Works Dataset

```json
[
  {
    "workId": "hamlet",
    "title": "Hamlet",
    "variables": ["hesitation_level"]
  },
  {
    "workId": "dracula",
    "title": "Dracula",
    "variables": ["vampire_nature"]
  },
  {
    "workId": "frankenstein",
    "title": "Frankenstein",
    "variables": ["creator_responsibility"]
  },
  {
    "workId": "pride_prejudice",
    "title": "Pride and Prejudice",
    "variables": ["first_impression_bias"]
  },
  {
    "workId": "don_quixote",
    "title": "Don Quixote",
    "variables": ["perception_of_reality"]
  }
]
```

---

## 🔁 Variation Object

```json
{
  "variationId": "var_001",
  "workId": "hamlet",
  "changes": [
    {
      "variableId": "hesitation_level",
      "newValue": 2
    }
  ],
  "newPremise": "A decisive prince acts quickly.",
  "causalSummary": [
    "Faster action",
    "Less internal conflict",
    "Earlier climax"
  ]
}
```

---

## 🔄 Engine Flow

1. User selects work
2. User modifies variables
3. System validates constraints
4. Decision graph recalculates
5. Narrative is generated
6. Comparison is displayed
7. User can vote / fork

---

## 🚀 MVP Recommendation

Start with 5 works:

* Hamlet
* Dracula
* Frankenstein
* Pride and Prejudice
* Don Quixote

Each with:

* 3–5 variables
* 3 characters
* 4 decision nodes

---

## 📈 Strategic Advantage

byDebut is not a content platform.

It is:

* a narrative simulation engine
* a creative decision system
* a scalable storytelling infrastructure

---

## ⚖️ Disclaimer

This platform generates original narratives based on abstracted structures and does not reproduce copyrighted text.

---

## 🧭 Next Steps

* Build API endpoints
* Connect UI sliders to variables
* Implement variation generator
* Add ranking + fork system

---

END OF FILE
