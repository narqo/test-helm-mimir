# Example

Running Mimir with meta-monitoring.

## Step 1. Spawn local Kubernetes cluster

```
% colima start --kubernetes

% colima ls
PROFILE    STATUS     ARCH       CPUS    MEMORY    DISK     RUNTIME       ADDRESS
default    Running    aarch64    4       8GiB      60GiB    docker+k3s
```

## Step 2. Install Mimir with Helm

See [mimir](./mimir).

## Step 3. Install Loki with Helm

See [loki](./loki).

Here, Loki is only needed to collect Mimir logs (via k8s-monitoring).

## Step 4. Install meta-monitoring with Helm

See [meta-monitoring](./meta-monitoring).

---

Optional

## Install tns-demo app

```
% git clone git@github.com:grafana/tns.git ; cd tns

···

# Using app-only
% ./install colima app-only
```

## Install Alloy with Helm

See [alloy](./alloy).
