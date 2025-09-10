# Contributing to SETSUNA

Thank you for your interest in contributing to SETSUNA! This document provides guidelines and instructions for contributing to the project.

## 🎯 How to Contribute

### Reporting Bugs
1. **Check existing issues** to avoid duplicates
2. **Use the bug report template** when creating new issues
3. **Include reproduction steps** and environment details
4. **Add relevant labels** (bug, high-priority, etc.)

### Suggesting Features
1. **Search existing feature requests** first
2. **Use the feature request template**
3. **Explain the use case** and expected behavior
4. **Consider the scope** - is this core to SETSUNA's mission?

### Code Contributions
1. **Fork the repository** and create a feature branch
2. **Follow the development setup** instructions in README.md
3. **Write tests** for new features
4. **Follow the code style** guidelines below
5. **Submit a pull request** with clear description

## 🛠 Development Setup

### Prerequisites
- Node.js 18+
- pnpm (recommended) or npm
- Docker (for local database)
- Git

### Local Environment
```bash
# Clone your fork
git clone https://github.com/yourusername/setsuna.git
cd setsuna

# Install dependencies
pnpm install

# Copy environment variables
cp .env.example .env.local
# Fill in your API keys and database URLs

# Set up database
pnpm db:push
pnpm db:seed

# Start development server
pnpm dev
```

### Testing
```bash
# Run all tests
pnpm test

# Run tests in watch mode
pnpm test:watch

# Run tests with coverage
pnpm test:coverage

# Type checking
pnpm type-check

# Linting
pnpm lint
```

## 📝 Code Style Guidelines

### TypeScript
- **Use TypeScript** for all new code
- **Define interfaces** for complex objects
- **Use type annotations** where TypeScript can't infer
- **Prefer `const assertions`** for literal types

### React Components
- **Use functional components** with hooks
- **Implement proper prop types** with TypeScript
- **Follow the single responsibility principle**
- **Use meaningful component and prop names**

### File Organization
```
src/
├── components/
│   ├── ui/           # Base UI components
│   ├── anime/        # Anime-specific components
│   └── shared/       # Reusable business components
├── app/              # Next.js app router pages
├── lib/              # Utilities and configurations
└── types/            # TypeScript type definitions
```

### Naming Conventions
- **Components**: PascalCase (`AnimeCard`, `UserProfile`)
- **Files**: kebab-case (`anime-card.tsx`, `user-profile.tsx`)
- **Variables/Functions**: camelCase (`getUserData`, `animeList`)
- **Constants**: SCREAMING_SNAKE_CASE (`API_ENDPOINTS`, `DEFAULT_SETTINGS`)

### Code Formatting
We use Prettier and ESLint for consistent formatting:
```bash
# Format code
pnpm format

# Check formatting
pnpm format:check

# Fix linting issues
pnpm lint:fix
```

### Database Changes
- **Use Prisma migrations** for schema changes
- **Test migrations** on sample data
- **Document breaking changes** in pull requests
- **Consider backward compatibility**

## 🔄 Pull Request Process

### Before Submitting
- [ ] **Tests pass** (`pnpm test`)
- [ ] **No TypeScript errors** (`pnpm type-check`)
- [ ] **No linting errors** (`pnpm lint`)
- [ ] **Code is formatted** (`pnpm format:check`)
- [ ] **Database changes are migrated** (`pnpm db:push`)

### PR Template
Use this template for your pull requests:

```markdown
## Description
Brief description of what this PR does.

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## Testing
- [ ] Unit tests pass
- [ ] Integration tests pass
- [ ] Manual testing completed

## Checklist
- [ ] My code follows the project's style guidelines
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
```

### Review Process
1. **Automated checks** must pass (tests, linting, type checking)
2. **Code review** by at least one maintainer
3. **Testing** on a staging environment
4. **Approval** and merge by maintainer

## 🏷 Commit Convention

We follow the [Conventional Commits](https://conventionalcommits.org/) specification:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Types
- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that do not affect the meaning of the code
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing tests or correcting existing tests
- **chore**: Changes to the build process or auxiliary tools

### Examples
```
feat(auth): add Discord OAuth integration

fix(ratings): prevent duplicate rating submissions

docs(api): update recommendation endpoint documentation

refactor(components): extract common button styles

test(anime): add unit tests for search functionality
```

## 🌟 Feature Development Process

### 1. Planning Phase
- **Create an issue** describing the feature
- **Discuss scope and approach** with maintainers
- **Get approval** before starting significant work

### 2. Development Phase
- **Create a feature branch** from `main`
- **Work in small, focused commits**
- **Write tests alongside code**
- **Update documentation** as needed

### 3. Review Phase
- **Self-review** your changes
- **Test thoroughly** (unit, integration, manual)
- **Submit pull request** with detailed description
- **Address review feedback**

## 🧪 Testing Guidelines

### Unit Tests
- **Test components** in isolation
- **Mock external dependencies** (APIs, database)
- **Cover edge cases** and error conditions
- **Use meaningful test descriptions**

### Integration Tests
- **Test user flows** end-to-end
- **Test database interactions**
- **Test API endpoints**
- **Use realistic test data**

### Testing Tools
- **Jest** for unit and integration tests
- **React Testing Library** for component testing
- **Playwright** for end-to-end testing (coming soon)
- **MSW** for API mocking

## 🚀 Deployment & Release Process

### Development Workflow
1. **Feature branches** merged to `develop`
2. **Continuous integration** runs tests
3. **Preview deployments** for testing
4. **Weekly releases** to production

### Release Process
1. **Version bump** using semantic versioning
2. **Update changelog** with new features and fixes
3. **Create release tag** and GitHub release
4. **Deploy to production** via Vercel

## 📞 Getting Help

### Discord Community
Join our Discord server for real-time discussions:
- **#dev-general**: General development questions
- **#feature-requests**: Discuss new features
- **#bug-reports**: Report and discuss bugs

### GitHub Discussions
Use GitHub Discussions for:
- **Architecture decisions**
- **Long-form technical discussions**
- **Community feedback**

### Maintainer Contact
- **@yourusername** - Project Lead
- **@contributor1** - Frontend Specialist
- **@contributor2** - Backend & AI

## 🎉 Recognition

Contributors are recognized in:
- **README.md** contributors section
- **Release notes** for significant contributions
- **Annual contributor appreciation** posts

Thank you for helping make SETSUNA the best anime platform possible! 🌟