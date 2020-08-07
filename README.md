Files related to this comment: https://github.com/webpack/webpack/issues/9802#issuecomment-670264258

Names should hopefully be obvious the "fscache" ones are with the filesystem cache configured:

```
cache: {
    type: 'filesystem',
    buildDependencies: {
        config: [__filename], // you may omit this when your CLI automatically adds it
    },
},
```

The "memcache" ones are with `cache: 'memory'`.

In both cases there were three compilations: initial, and two no-op file changes (`touch` of the entry point JS file).