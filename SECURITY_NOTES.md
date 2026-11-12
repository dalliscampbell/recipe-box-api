#Security notes
2026-11-12

- GET /recipes → Anonymous requester can read all recipes, including ones with "is_public": false.
- PATCH /recipes/3 → Anonymous requester can change any recipe; change persisted when re-fetching.
- DELETE /recipes/3 → Anonymous requester can delete any recipe; recipe no longer appears in GET /recipes.