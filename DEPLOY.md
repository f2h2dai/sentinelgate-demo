# Publish with GitHub CLI (PowerShell)

```powershell
cd C:\AI\sentinelgate-demo

git init
git add .
git commit -m "Publish SentinelGate demo"
git branch -M main

gh repo create f2h2dai/sentinelgate-demo --public --source=. --remote=origin --push

gh api --method POST repos/f2h2dai/sentinelgate-demo/pages `
  -f build_type=legacy `
  -f 'source[branch]=main' `
  -f 'source[path]=/'
```

If Pages already exists, use:

```powershell
gh api --method PUT repos/f2h2dai/sentinelgate-demo/pages `
  -f build_type=legacy `
  -f 'source[branch]=main' `
  -f 'source[path]=/'
```
