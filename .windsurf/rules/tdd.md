---
description: 
globs: 
alwaysApply: false
---
# TDD (Test-Driven Development) Rules

## Core Principles

- **Red-Green-Refactor** cycle
- Write tests before implementation
- Take small, incremental steps
- Write tests for all features

## Development Cycle

### 1. Red (Write a failing test)

- Clearly understand the feature requirements
- Write a minimal failing test
- Make tests specific and easy to understand

### 2. Green (Implement minimal code to pass)

- Implement minimal code to pass the test
- It's okay if it's not perfect
- Break down complex problems into simple steps

### 3. Refactor (Improve code quality)

- Improve code quality (DRY, SOLID principles)
- Ensure tests continue to pass
- Avoid technical debt

## Test Structure

### Unit Tests

- Test functions/methods individually
- Mock external dependencies
- Place in `/src/components/__tests__/` or `/src/__tests__/`

### Integration Tests

- Test multiple components/modules integration
- Place in `/src/tests/integration/`
- Use MSW for API mocking

### E2E Tests

- Simulate user interactions
- Place in `/e2e/`
- Focus on critical user paths

## Testing Tools

- **Jest**: Test runner
- **React Testing Library**: Component tests
- **Cypress/Playwright**: E2E tests
- **MSW**: API mocking

## Naming Conventions

- Test files: `[feature].test.ts` or `*.spec.ts`
- Test suites: `describe('Component', ...)`
- Place mocks in `__mocks__`

## Coverage

- Minimum 80% coverage
- Output to `/coverage/` directory
- Aim for 100% coverage for business logic

## CI/CD Integration

- Run tests on every PR
- Check coverage in CI
- Block merge on test failures

## Mocks and Dependencies

- Replace external API/DB with mocks
- Create fresh test data using factory functions
- Manage environment variables in `.env.test`

## Performance

- Optimize tests for speed
- Optimize slow tests
- Run tests in parallel
- Optimize test data setup and cleanup

## Notes

- Don't change code for tests
- Test behavior, not implementation details
- Use snapshot tests with caution
