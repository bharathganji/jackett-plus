# Contributing to Jackett Plus

Thank you for your interest in contributing to **Jackett Plus**! We welcome bug reports, feature requests, documentation improvements, and code contributions.

---

## Code of Conduct

All contributors are expected to uphold our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

---

## Monorepo Architecture

`jackett-plus` is organized as a unified monorepo:

- **`docker-compose.yml`**: Stack orchestrator binding all services into the VPN network namespace.
- **`vpn/`**: OpenVPN client configuration (`vpn.conf`).
- **`services/api/`**: Asynchronous FastAPI streaming backend (Python 3.12, Uvicorn, Server-Sent Events).
- **`services/ui/`**: Modern React 19 web application (TypeScript, Tailwind CSS, Vite, TanStack Virtual).

---

## Development Workflow

### Prerequisites
- Docker & Docker Compose v2+
- Python 3.12+ (for local backend development)
- Node.js 22+ & npm 9+ (for local frontend development)

### Setting Up Local Environment
1. Fork and clone the repository:
   ```bash
   git clone https://github.com/<your-username>/jackett-plus.git
   cd jackett-plus
   ```
2. Copy environment template:
   ```bash
   cp .env.example .env
   ```
3. Run the development stack:
   ```bash
   docker compose up -d --build
   ```

---

## Testing & Quality Assurance

Before submitting a Pull Request, ensure all tests and lint checks pass:

### Backend Tests (Python)
```bash
cd services/api
pip install -r requirements.txt
pytest
```

### Frontend Build & Lint (Node.js)
```bash
cd services/ui
npm ci
npm run build
npm run lint
```

### Docker Compose Validation
```bash
docker compose config --quiet
```

---

## Commit Message Guidelines (Conventional Commits)

We enforce the [Conventional Commits](https://www.conventionalcommits.org/) specification for automated semantic versioning and changelog generation:

Format: `<type>(<scope>): <subject>`

### Types
- `feat`: A new feature (triggers `minor` release)
- `fix`: A bug fix (triggers `patch` release)
- `perf`: Performance improvement (triggers `patch` release)
- `refactor`: Code refactoring without behavior change
- `docs`: Documentation updates only
- `test`: Adding or updating test suites
- `chore`: Maintenance tasks, dependencies, build configs

### Breaking Changes
Include `BREAKING CHANGE: <description>` in the commit body or footer to trigger a `major` release.

---

## Pull Request Process

1. Create a feature or fix branch from `main`:
   ```bash
   git checkout -b feat/my-new-feature
   ```
2. Commit your changes adhering to Conventional Commits.
3. Verify all automated tests pass locally.
4. Push your branch to your fork and submit a Pull Request against `main`.
5. Ensure all CI checks (tests, linting, Gitleaks secret scanner) pass on GitHub Actions.
