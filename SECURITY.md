# Security / Privacy

This repository must not contain any secrets or personal data.

## Do NOT commit
- API keys, tokens, passwords
- IP addresses, hostnames, usernames
- Full logs that may include headers/cookies/auth
- Any .env, config dumps, or command history

## Before every push
Run:
  grep -RInE --exclude-dir=.git 'ghp_[A-Za-z0-9]{20,}|API[_-]?KEY|Authorization: Bearer|token|secret|OPENAI|OPENROUTER|BRAVE|TAVILY' .

If anything matches, redact it and re-check.

## If a secret is exposed
Immediately revoke/rotate the secret, then rewrite git history if needed.
