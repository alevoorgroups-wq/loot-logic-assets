# Loot Logic Assets

Public assets for the [Loot Logic](https://github.com/alevoorgroups-wq/loot-logic) YouTube channel pipeline.

This repo exists for one reason: some external APIs (like Pollinations' `kontext` image-to-image model) need a genuinely public URL to fetch a reference image from. The main `loot-logic` repo is private and stays that way - `raw.githubusercontent.com` returns 404 for private-repo content to unauthenticated requests, which external services can't work around. This repo holds only the specific images that need to be fetchable that way; all business logic, prompts, and pipeline code remain in the private repo.

## Contents

- `mascot/reference.png` - the locked reference image for the comics-pillar mascot character. Used as the identity anchor for every `kontext` scene generation. Do not replace this file without updating `scripts/mascot_generator.py` in the main repo - every future scene generation depends on this exact file.
