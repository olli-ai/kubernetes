# kube-scheduling

This is a fork of https://github.com/kubernetes/kubernetes in order to patch `kube-scheduler:1.14.10`. The latter bugs when pods are updated by [`gpu-admission`](https://github.com/olli-ai/gpu-admission).

# build

The building process is a nightmare

Install `bazel-2.2.0`
```bash
curl https://bazel.build/bazel-release.pub.gpg | sudo apt-key add -
echo "deb [arch=amd64] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
sudo apt update && sudo apt install bazel-2.2.0
```

Build mostly everything (it takes forever)
```bash
make quick-release
```

Create the image and push it
```bash
cd kube-scheduler
make VERSION=my-version
```
