# Getting Started with SymPress

For new users, the intended path is:

1. **Explore the demo.** [`sympress/demo`](https://github.com/SymPress/demo)
   shows the architecture in a real WordPress site — kernel, assets,
   migrations, ORM, logging, profiler, blocks, admin UI, and REST all in
   context.
2. **Create a project.** Use [`sympress/cli`](https://github.com/SymPress/cli)
   and [`sympress/starter`](https://github.com/SymPress/starter) to scaffold
   a DDEV-ready Composer project.
3. **Start with the foundation packages.** Kernel, framework bundle, assets,
   migrations, and events — see the [full package map](packages.md).
4. **Add developer-experience packages as needed.** Monolog, profiler,
   WP-CLI console, maker, and asset compiler.
5. **Add business packages once the platform layer is stable.** Mailer,
   consent, forms, automation, and integrations as they become available.

Each package can be adopted on its own — you don't need the full stack to
get value from any single one.
