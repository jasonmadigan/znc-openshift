# ZNC on OpenShift

Create a new project:

```bash
oc new-project znc
```

OR switch to an existing one:

```bash
oc project znc
```

Next, create the ZNC app and all its supporting resources:

```bash
oc new-app -f znc-template.yaml
```

Find the public route for your new app:

```bash
oc get route/znc
```

Open the ZNC web console at your route's URL, e.g. `https://znc-myapp.openshift.example.com`. Log in with the default admin account (username/password: `admin`).


## Install thelounge

https://thelounge.github.io/

```bash
oc new-app -f thelounge-template.yaml
```

Find the public route for thelounge:

```bash
oc get route/thelounge
```
