## Register new GitHub App

Register a domain, `<domain name>` from here on out, and point it at your load balancer.

Configure your load balancer to get an SSL key for heckler.<domain name>

Head over to https://github.com/settings/apps/new

Name the app, give it a URL, like heckler's homepage or the fork, if that's the plan.

Create a github repo with all your puppet files in it.

```
ssh-keygen -t rsa -b 4096 -m PEM -f github_hecklerd
```

Don't use a password.

Upload the key as a deploy key for your puppet repo.
