# Roadmap & Current Focus

## Current Focus

The product roadmap is moving in four tracks:

1. Stabilize the foundation packages.
2. Make project creation and local development fast enough to try in
   minutes.
3. Build a realistic demo that explains the architecture in context.
4. Add higher-level packages for templates, data, mail, consent, forms,
   automation, and integrations.

Follow the live public board here: [SymPress Roadmap](https://github.com/orgs/SymPress/projects/1).

## Kernel Architecture Notes

`sympress/kernel` is the foundation package. It is no longer just a thin
shared container idea; it is the site-level application kernel for
Composer-based WordPress projects.

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

> This section tracks the kernel's architectural direction at the org level.
> For implementation details, see the [`sympress/kernel`](https://github.com/SymPress/kernel)
> README directly.

## Near-Term Work

- finish the first foundation release train
- publish and auto-update packages on Packagist
- align README, changelog, security, and contribution files across
  repositories
- document supported PHP, WordPress, and Symfony versions
- keep the demo project installable from public packages
- improve the CLI and starter flow for first project creation

## Longer-Term Work

- stabilize the public kernel, bundle, hook, config, route, and package
  discovery APIs
- expand the demo with realistic admin, block, REST, data, mail, and
  profiling flows
- bring business packages such as mailer, consent, forms, automation, and
  integrations onto the same release standard
- define a clear support policy for stable releases
