A dummy bosh release to demonstrate https://github.com/cloudfoundry/bpm-release/issues/128

The release defines two dummy jobs:
* `rep` which creates a directory in its bpm-pre-start script
* `garden` which has the directory created by `rep` as a shared mounted BPM
  volume

In order to deploy the release on a bosh-lite one should run

```
./scripts/deploy-lite-rootless.sh
```

To recreate the deployment:

```
./scripts/deploy-lite-rootless.sh --recreate

```
