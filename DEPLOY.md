# Update the existing SentinelGate GitHub Pages demo

Existing repository: `f2h2dai/sentinelgate-demo`

From your local repository:

```powershell
cd C:\AI\sentinelgate-github-pages\sentinelgate-github-pages

# Copy the redesigned files into this folder first, then:
git status
git add index.html README.md DESIGN.md .nojekyll
git commit -m "Apply SentinelGate DESIGN.md and review-workspace redesign"
git push
```

GitHub Pages is already configured from `main` at `/`. Pushing to `main` triggers a rebuild.

Live demo:

`https://f2h2dai.github.io/sentinelgate-demo/`
