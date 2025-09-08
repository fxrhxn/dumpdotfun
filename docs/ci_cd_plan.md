# CI/CD Plan – Dump.fun Platform

## 1. Testing Commits
- All commits must pass linting & unit tests before merge
- Run tests locally before pushing

## 2. Linting Commands
- Frontend: `npx eslint . --fix`
- Smart Contracts: `cargo clippy --workspace`

## 3. Unit Test Execution
- Frontend: `npm test`
- Smart Contracts: `anchor test`

## 4. Deployment Workflow
- Scripts stored in `scripts/` folder
- Devnet deployment: `scripts/deploy_devnet.sh`
- Testnet deployment: `scripts/deploy_testnet.sh`
- Steps:
  1. Run smart contract tests
  2. Lint & test frontend
  3. Deploy contracts via scripts
  4. Push frontend updates if necessary

## 5. CI/CD Automation (Optional)
- GitHub Actions placeholder: `.github/workflows/ci.yml`
