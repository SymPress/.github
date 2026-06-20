# Where SymPress Fits

WordPress has a large, mature ecosystem for project skeletons, environment
management, and frontend tooling. SymPress is not a replacement for any of
that — it is the architecture layer most of those tools intentionally leave
out: dependency injection, a compiled service container, and testable
package boundaries.

The table below compares SymPress to the tools people most often ask about.
In most real projects, SymPress is used *alongside* these tools rather than
instead of them.

| | SymPress | Bedrock | Sage | Plain Composer-managed WordPress | Headless WordPress |
| --- | --- | --- | --- | --- | --- |
| **What it provides** | Application kernel, dependency injection, declarative hooks, routing, migrations | Project skeleton, `.env`-based config, modern folder layout | Theme tooling, modern frontend build (Vite/Webpack) | Composer autoloading only | WordPress as a pure data API |
| **Dependency injection** | Yes — Symfony's container | No | No | No | Depends on the chosen app framework |
| **WordPress stays the runtime** | Yes | Yes | Yes | Yes | No — WordPress becomes a backend service only |
| **Adoption** | Incremental, one package at a time | Usually a project-start decision | Usually a theme-start decision | N/A | Full rearchitecture |
| **Testability** | High — services and hooks can be unit tested in isolation | Unchanged from core WordPress | Unchanged from core WordPress | Low, without extra discipline | High, but loses WordPress's content/admin workflows |
| **Works together with SymPress?** | — | Yes, commonly paired | Yes, commonly paired | Yes — it's a reasonable starting point | No — different architectural direction entirely |
| **Choose this when...** | Your team knows Symfony/DI patterns and is building or maintaining a WordPress application that's outgrowing single-plugin structure | You want a clean, modern project skeleton and don't need a service container | You're building a custom theme with a modern frontend toolchain | The project is small and doesn't need application-level structure | You're intentionally leaving WordPress's rendering and admin behind |

## In short

- **Bedrock** answers *"how is my project laid out?"* SymPress answers
  *"how do my services talk to each other?"* They solve different problems
  and combine cleanly.
- **Sage** answers the same kind of question for themes and frontend builds —
  also fully compatible.
- **Headless WordPress** is a different bet entirely: you're trading
  WordPress's admin and content workflows for a clean API boundary. SymPress
  assumes you want to keep those, just with better internals underneath.

If you're already happy with how your WordPress project is laid out and just
want services that don't depend on global functions and `add_action()` soup —
that's exactly the gap SymPress fills.
