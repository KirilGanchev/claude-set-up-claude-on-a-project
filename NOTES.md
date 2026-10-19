I put this in claude.md:
Commands — at least two you run often (here: npm run dev, npm test, npm run lint)
Conventions — at least two real rules ("use X, not Y"), written so Claude can follow them without asking a question
Architecture — a few lines on how the project is organised (the server.js entry point, one route file per resource in routes/, data access through db/store.js)

I put this in .claude/settings.json:
{
  "permissions": {
    "allow": ["Bash(npm test:*)"],
    "ask": ["Bash(git push:*)"],
    "deny": ["Read(./.env)", "Bash(git push --force:*)"]
  }
}

Everything was checked and verified with /memory and /permissions