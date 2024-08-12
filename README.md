# My loco test project :train:

Loco is a web and API framework running on Rust.

This is my test project bootstrapped with the **SaaS starter** which includes a `User` model and authentication based on JWT.

## Prerequisites

You will need:

- [rust](https://www.rust-lang.org/tools/install)
- [pnpm](https://pnpm.io/fr/installation) recommended to install via [volta](volta.sh)
- [podman](https://podman.io/) to run containers (db and queue)

## Quick Start

Start the Postgres and Redis instance by running `podman compose up -d`

Verify everything works by running `cargo loco doctor`

The first time you will have to build the frontend project:

```sh
cd frontend 
pnpm install
pnpm build
```

Go back to the root directory and start the server `cargo loco start`

You can also run it in watch mode with `cargo-watch`, which will give you server hot reloading

```sh
cargo-watch -x check  -s 'cargo loco start'
```

For the frontend use `pnpm dev` for HMR (hot module reloading)
