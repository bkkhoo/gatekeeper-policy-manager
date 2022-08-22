Deploy [Gatekeeper Policy Manager](https://github.com/sighupio/gatekeeper-policy-manager) with [openshift-oauth-proxy](https://github.com/openshift/oauth-proxy):
```
session_secret=$(echo -n $RANDOM | md5sum | head -c 24)  oc -n openshift-gatekeeper-system apply -k gatekeeper-policy-manager/
```

**Note**:
* the manifests deploy GPM on OpenShift cluster, which uses `openshift-gatekeeper-system` instead of `gatekeeper-system` namespace.
* openshift-oauth-proxy is a fork of https://github.com/oauth2-proxy/oauth2-proxy
