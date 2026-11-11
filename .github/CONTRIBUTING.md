# Contributing to ERP-System

Thanks for your interest in improving **ERP-System**, a centralised system for streamlining and automating construction operations. Bug reports, fixes, docs and new features are all welcome.

**Stack:** Node.js · Express · MongoDB · React

## Ways to contribute

- 🐛 **Report a bug:** [open a bug report](https://github.com/khemssharma/ERP-System/issues/new?template=bug_report.yml)
- 💡 **Suggest a feature:** [open a feature request](https://github.com/khemssharma/ERP-System/issues/new?template=feature_request.yml)
- 📝 **Improve the docs:** typos, unclear steps and missing examples all count
- 🔧 **Fix an issue:** look for issues labelled `good first issue` or `help wanted`

For anything bigger than a small fix, please **open an issue first**, so we can agree on the approach before you spend time on it.

## Local setup

```bash
git clone https://github.com/<your-username>/ERP-System.git
cd ERP-System
npm install
cd backend && npm install && cd ..
cd frontend && npm install && cd ..
# create backend/.env (MongoDB URI, JWT secret, port)
npm run dev                 # runs backend and frontend together
```

You can also run them separately with `npm run server` and `npm run client`.

## Project layout

| Path | What lives there |
| --- | --- |
| `backend/` | Express API and MongoDB models |
| `frontend/` | React client |

## Making a change

1. **Fork** the repo and create a branch from `master`:
   ```bash
   git checkout -b feat/short-description   # or fix/…, docs/…, refactor/…
   ```
2. Make your change. Keep each PR focused on **one** thing.
3. Run the checks below.
4. Commit using [Conventional Commits](https://www.conventionalcommits.org/):
   ```
   feat: add rematch button
   fix: handle disconnect during game
   docs: clarify .env setup
   ```
5. Push to your fork and open a pull request against `master`. Fill in the PR template.

## Checks before you open a PR

```bash
npm test                    # runs the test suites
(cd frontend && npm run build)   # frontend must build
```

## Project-specific guidelines

- **Data model changes:** describe any change to MongoDB schemas in the PR and how existing records are handled.
- **Roles and permissions:** if your change touches who can see or edit data (sites, workers, materials, finances), say so clearly in the PR.
- **Never commit** `.env` files, real company data or credentials.

## Code style

- Match the style of the code around your change.
- Use clear, descriptive names; avoid unexplained abbreviations.
- Remove debug logs and commented-out code before committing.
- Update the README if your change affects setup or usage.

## Reporting security issues

Please **don't open a public issue** for security vulnerabilities. Contact the maintainer privately through the [GitHub profile](https://github.com/khemssharma) with the details and steps to reproduce.

## Code of conduct

Be respectful and constructive. Harassment, personal attacks and spam aren't tolerated.

## License

This repository doesn't have an open-source license yet. Until one is added, by submitting a contribution you agree that it may be used, modified and distributed as part of this project.
