# SentinelGate public demo

A static public demo of the SentinelGate agent acceptance and assurance workspace.

## Design authority

`DESIGN.md` is the canonical visual design contract. UI changes must follow it.

## Public-demo boundary

- Synthetic records only
- No production connections
- No credentials
- No customer or internal evidence
- No operational agent execution

## Local preview

```powershell
python -m http.server 8787 --bind 127.0.0.1
```

Open `http://127.0.0.1:8787`.
