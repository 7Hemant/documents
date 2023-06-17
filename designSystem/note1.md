# introduction to design system

# Do you need a design system?

Despite the hype, a design system isn’t a silver bullet. If you work with a modest team on a single app, you’re better off with a directory of UI components instead of setting up the infrastructure to enable a design system. For small projects, the cost of maintenance, integration, and tooling far outweighs any productivity benefits you might see.

The economy of scale in a design system works in your favor when sharing UI components across many projects. If you find yourself pasting the same UI components in different apps or across teams, this guide is for you.

# What we’re building

## We’ll be building the following frontend stack:

-     Build components
  - 📚 Storybook for UI component development and auto-generated docs
  - ⚛️ React for declarative component-centric UI (via create-react-app)
  - 💅 Styled-components for component-scoped styling
  - ✨ Prettier for automatic code formatting
-     Maintain the system
  - 🚥 GitHub Actions for continuous integration
  - 📐 ESLint for JavaScript linting
  - ✅ Chromatic to catch visual bugs in components (by Storybook maintainers)
  - 📦 npm for distributing the library
  - 🛠 Auto for release management workflow
-      Storybook addons

  - ♿ Accessibility to check for accessibility issues during development
  - 💥 Actions to QA click and tap interactions
  - 🎛 Controls to interactively adjust props to experiment with components
  - 📕 Docs for automatic documentation generation from stories
  - 🔍 Interactions for debugging component interactions
  - 🏎 Test-runner for automated component testing

  # why we need a design system

  - _It is built to address having to paste the same components into multiple projects again and again._
