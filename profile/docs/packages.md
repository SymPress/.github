# Package Map

SymPress is split into small, composable Composer packages. Adopt them one
at a time — you don't need all of them to get value from any single one.

## Foundation

These packages define the runtime shape and release train.

| Repository | Role |
| --- | --- |
| [`sympress/kernel`](https://github.com/SymPress/kernel) | Site kernel, shared service container, bundle discovery, hooks, routes, config, and console integration. |
| [`sympress/framework-bundle`](https://github.com/SymPress/framework-bundle) | Symfony FrameworkBundle bridge, framework services, cache pools, and WordPress object-cache support. |
| [`sympress/assets`](https://github.com/SymPress/assets) | Structured script, style, module, manifest, and asset registration for WordPress packages. |
| [`sympress/migration`](https://github.com/SymPress/migration) | Versioned database and project migrations for WordPress sites and packages. |
| [`sympress/event-dispatcher`](https://github.com/SymPress/event-dispatcher) | Class-based events, listeners, subscribers, and WordPress hook event flows. |

## Application Layer

These packages make SymPress useful for real application code.

| Repository | Role |
| --- | --- |
| [`sympress/twig-bundle`](https://github.com/SymPress/twig-bundle) | Twig integration with Symfony TwigBundle compatibility, template discovery, extensions, and globals. |
| [`sympress/orm`](https://github.com/SymPress/orm) | Doctrine-inspired ORM primitives for WordPress projects that keep `wpdb` as the database runtime. |

## Developer Experience

These repositories help teams create, inspect, test, and ship SymPress
projects.

| Repository | Role |
| --- | --- |
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

## Business Building Blocks

The next product layer focuses on recurring business workflows that should
be testable, consent-aware, and easy to integrate with project code.

Planned or in-progress areas include:

- `sympress/mailer` for Symfony Mailer-powered WordPress email
- `sympress/mailer-pro` for routing, logging, queueing, reports, alerts, and
  operational controls
- `sympress/consent` for consent-aware scripts, embeds, and asset loading
- forms and submission inboxes for code-first form handling
- double opt-in and preference-center flows
- automation for event-driven business workflows
- integrations for webhooks, CRMs, analytics, and external systems
