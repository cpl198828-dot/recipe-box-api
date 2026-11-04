# Security baseline

## 2026-11-02

- Anonymous `GET /recipes` returns all recipes, including ones with `is_public: false`, such as "Secret family hot sauce".
- Anonymous `PATCH /recipes/2` successfully changed the title to "Totally hacked oats".
- Anonymous `DELETE /recipes/2` removed recipe 2; subsequent `GET /recipes/2` returns `{"error": "recipe not found"}`.
