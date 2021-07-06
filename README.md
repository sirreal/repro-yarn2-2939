Reproduction repo for https://github.com/yarnpkg/berry/issues/2939

This has been reduced to a minimal public test case. The original issue manifests when using an
private npm registry.

To reproduce:

```sh
yarn dedupe
```

The lockfile is valid:

```sh
yarn install --immutable
```

The issue exists on latest (as of https://github.com/yarnpkg/berry/commit/fce9eb661522bb3989a5eb0c1b3f87027f8a3970):

```sh
yarn set version from sources
yarn install --immutable
yarn dedupe
```
