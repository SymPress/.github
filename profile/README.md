### SymPress

<p align="center">
  <img src="https://raw.githubusercontent.com/SymPress/.github/main/profile/header.png" alt="SymPress banner" width="100%">
</p>

SymPress brings Symfony architecture into professional WordPress projects
without hiding WordPress or replacing its runtime. WordPress stays the CMS,
admin, plugin ecosystem, hooks layer, and publishing platform. SymPress adds the
application structure larger Composer-based projects usually need: a kernel,
dependency injection, bundle discovery, configuration, events, migrations,
assets, console tooling, logging, profiling, templates, and testable package
boundaries.

The project is in active pre-release development. Public repositories are being
prepared for stable Composer releases, clearer documentation, Packagist
publishing, and a repeatable demo/start-project workflow.

## What SymPress Builds

- A Symfony-powered application layer for WordPress websites, plugins, MU
  plugins, and themes.
- Reusable Composer packages that can be adopted one at a time.
- A shared developer experience for service-oriented WordPress projects.
- Reference tooling for local setup, quality checks, CI, releases, and demos.
- Business-ready building blocks that can grow on top of the platform.

## Current Focus

The product roadmap is moving in four tracks:

1. Stabilize the foundation packages.
2. Make project creation and local development fast enough to try in minutes.
3. Build a realistic demo that explains the architecture in context.
4. Add higher-level packages for templates, data, mail, consent, forms,
   automation, and integrations.

## Kernel Update

`sympress/kernel` is the foundation package. It is no longer just a thin shared
container idea; it is the site-level application kernel for Composer-based
WordPress projects.

The kernel now centers on:

- one shared application container per site
- Composer package and bundle discovery through `extra.kernel` metadata
- Symfony-style service configuration, compiler passes, and autoconfiguration
- declarative WordPress hooks through attributes or service tags
- Symfony DI attributes such as autowiring, locators, aliases, decorators,
  conditions, lazy services, required dependencies, and resource tags
- Symfony-style routes for frontend and REST endpoints
- console command discovery through the kernel console integration
- compiled, cached runtime containers with deployment-aware invalidation
- optional package-manager inspection for Composer-backed WordPress packages

## Package Map

### Foundation

These packages define the runtime shape and release train.

| Repository | Role |
| :--- | :--- |
| [`sympress/kernel`](https://github.com/SymPress/kernel) | Site kernel, shared service container, bundle discovery, hooks, routes, config, and console integration. |
| [`sympress/framework-bundle`](https://github.com/SymPress/framework-bundle) | Symfony FrameworkBundle bridge, framework services, cache pools, and WordPress object-cache support. |
| [`sympress/assets`](https://github.com/SymPress/assets) | Structured script, style, module, manifest, and asset registration for WordPress packages. |
| [`sympress/migration`](https://github.com/SymPress/migration) | Versioned database and project migrations for WordPress sites and packages. |
| [`sympress/event-dispatcher`](https://github.com/SymPress/event-dispatcher) | Class-based events, listeners, subscribers, and WordPress hook event flows. |

### Application Layer

These packages make SymPress useful for real application code.

| Repository | Role |
| :--- | :--- |
| [`sympress/twig-bundle`](https://github.com/SymPress/twig-bundle) | Twig integration with Symfony TwigBundle compatibility, template discovery, extensions, and globals. |
| [`sympress/orm`](https://github.com/SymPress/orm) | Doctrine-inspired ORM primitives for WordPress projects that keep `wpdb` as the database runtime. |

### Developer Experience

These repositories help teams create, inspect, test, and ship SymPress projects.

| Repository | Role |
| :--- | :--- |
| [`sympress/cli`](https://github.com/SymPress/cli) | Standalone CLI for creating and updating configured SymPress projects from starter manifests. |
| [`sympress/starter`](https://github.com/SymPress/starter) | DDEV-ready Composer project template for new SymPress WordPress websites. |
| [`sympress/demo`](https://github.com/SymPress/demo) | Reference WordPress website showing the kernel, assets, migrations, ORM, logging, profiler, blocks, admin UI, and REST in context. |
| [`sympress/maker-bundle`](https://github.com/SymPress/maker-bundle) | Package-aware Symfony MakerBundle integration for commands, hooks, blocks, config loaders, asset entries, and packages. |
| [`sympress/wp-cli-console`](https://github.com/SymPress/wp-cli-console) | Symfony Console patterns around useful WP-CLI workflows. |
| [`sympress/asset-compiler`](https://github.com/SymPress/asset-compiler) | Composer plugin for installing frontend dependencies and compiling package assets. |
| [`sympress/monolog-bundle`](https://github.com/SymPress/monolog-bundle) | Monolog integration for structured WordPress application logging. |
| [`sympress/profiler`](https://github.com/SymPress/profiler) | Development profiler and web debug toolbar for WordPress requests. |
| [`sympress/coding-standards`](https://github.com/SymPress/coding-standards) | PHP coding standards for scalable WordPress and Symfony-inspired development. |
| [`SymPress/workflows`](https://github.com/SymPress/workflows) | Shared GitHub Actions workflows for Composer, WordPress, Playwright, releases, deployments, and secure artifacts. |

### Business Building Blocks

The next product layer focuses on recurring business workflows that should be
testable, consent-aware, and easy to integrate with project code.

Planned or in-progress areas include:

- `sympress/mailer` for Symfony Mailer-powered WordPress email
- `sympress/mailer-pro` for routing, logging, queueing, reports, alerts, and
  operational controls
- `sympress/consent` for consent-aware scripts, embeds, and asset loading
- forms and submission inboxes for code-first form handling
- double opt-in and preference-center flows
- automation for event-driven business workflows
- integrations for webhooks, CRMs, analytics, and external systems

## Adoption Path

For new users, the intended path is:

1. Explore [`sympress/demo`](https://github.com/SymPress/demo) to see the
   architecture in a real WordPress site.
2. Create a project with [`sympress/cli`](https://github.com/SymPress/cli) and
   [`sympress/starter`](https://github.com/SymPress/starter).
3. Start with the foundation packages: kernel, framework bundle, assets,
   migrations, and events.
4. Add developer-experience packages such as Monolog, profiler, WP-CLI console,
   maker, and asset compiler as the project needs them.
5. Add business packages once the platform layer is stable.

## Principles

- WordPress remains the runtime.
- Symfony components provide structure where structure pays off.
- Packages should be small, composable, documented, and testable.
- Integration should improve maintainability without hiding WordPress behavior.
- Adoption should work one package at a time.

## What SymPress Is Not

SymPress is intentionally not:

- a replacement for WordPress
- a full-stack framework that hides WordPress
- a page builder
- a theme framework
- a plugin marketplace
- a reason to avoid learning WordPress APIs

The goal is to make WordPress projects more maintainable while keeping them
recognizably WordPress.

## Roadmap

Near-term work:

- finish the first foundation release train
- publish and auto-update packages on Packagist
- align README, changelog, security, and contribution files across repositories
- document supported PHP, WordPress, and Symfony versions
- keep the demo project installable from public packages
- improve the CLI and starter flow for first project creation

Longer-term work:

- stabilize the public kernel, bundle, hook, config, route, and package
  discovery APIs
- expand the demo with realistic admin, block, REST, data, mail, and profiling
  flows
- bring business packages such as mailer, consent, forms, automation, and
  integrations onto the same release standard
- define a clear support policy for stable releases

## Contributing

SymPress is built as an open project, and focused contributions are welcome.
Bug reports, feature ideas, documentation improvements, examples, tests, and
pull requests all help the project move forward.

If you are curious about modern WordPress architecture, Symfony components,
Composer-first workflows, or better developer experience for WordPress teams,
there is room to contribute. Start with the issue templates when opening new
work, and read the contribution guide before sending larger changes.

## Links

- :page_with_curl: [Contribution guide](../CONTRIBUTING.md)
- :lock: [Security policy](../SECURITY.md)
- :balance_scale: [License](../LICENSE)
