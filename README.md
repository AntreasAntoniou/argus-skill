# Argus

A durable-context checkpoint skill for Git-backed knowledge systems. Argus preserves only the delta that should outlive a conversation, routes each fact to one canonical owner, and validates logical backlinks across registered archives.

```bash
npx skills add AntreasAntoniou/argus-skill
export ARCHIVUM_REGISTRY=/path/to/00_meta/archivum_registry.toml
python3 scripts/discover_archivums.py --json
python3 scripts/check_backlinks.py --registry "$ARCHIVUM_REGISTRY"
```

The scripts are read-only. The skill never treats preservation authority as permission to publish, send, or broaden scope.

## Test

```bash
python3 -m unittest discover -s tests
```

MIT licensed.
