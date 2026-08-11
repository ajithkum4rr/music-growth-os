# Phase 0 — Security

## Goal

Document account security and data protection practices.

## Why this matters

Secure accounts protect your brand, marketing budget, and fan relationships.
A security incident can interrupt campaigns and damage trust.

## What this covers

- Password security
- Two-factor authentication (2FA)
- Account permissions
- Secrets and credentials handling

## Step-by-step

### Step 1 — use a password manager

Store all account credentials in a password manager.
Do not keep passwords in plain text files or in this repository.

### Step 2 — enable 2FA

Enable two-factor authentication on every platform that supports it.
Use an authenticator app if possible.

### Step 3 — assign least privilege

Give access only to people who need it.
Create separate accounts for ads, email, and distribution.

### Step 4 — handle API keys and tokens safely

- Use `.env.example` for placeholder configuration.
- Keep actual keys out of the repo.
- Store real secrets in secure vaults or environment variables.

### Step 5 — protect account recovery

Keep recovery email and phone details current.
Use secure recovery options, not easily guessable answers.

## What to record

- Which accounts have 2FA enabled.
- Which password manager you use.
- Notes on any delegated access.
- Where you store account recovery details.

## Common mistakes

- Storing credentials in repo files.
- Reusing the same password across accounts.
- Giving full access to people who only need limited access.
- Ignoring account recovery settings.

## Troubleshooting

- If a login is locked, follow the platform recovery process.
- If you suspect an account compromise, change access and rotate keys.
- If access is shared, audit permissions regularly.

## Notes

- Security is a continuous process.
- Review permissions and credentials at least quarterly.
