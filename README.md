# ZNC on OpenShift

Create a new project:

```bash
oc new-project znc
```

Or switch to an existing one:

```bash
oc project znc
```

Create the ZNC app and all its supporting resources:

```bash
oc new-app -f template.yaml
```

Find the public route for your new app:

```bash
oc get route/znc
```

Open the ZNC web console at your route's URL, e.g. `https://znc-myapp.openshift.example.com`. Log in with the default admin account (username/password: `admin`).
