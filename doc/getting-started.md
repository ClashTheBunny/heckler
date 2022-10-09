## Register new GitHub App

Register a domain, `<domain name>` from here on out, and point it at your load balancer.

Configure your load balancer to get an SSL key for heckler.<domain name>

Head over to https://github.com/settings/apps/new

Name the app, give it a URL, like heckler's homepage or the fork, if that's the plan.

### generate a private key (a pem file) on your github app

Go to https://github.com/settings/apps/heckler-dev#private-key and download the resulting key to `github-hecklerd.pem` in the root heckler directory.

Add the IP that heckler will reach out to the GitHub API with at the very bottom in the "IP allow list" section.

In the general settings for your app, copy the App ID and put it in hecklerd_conf.yaml.

Create a github repo with all your puppet files in it.

Add the heckler vendor directory from manifests/vendor/heckler to your basemodulespath somewhere

Add `,heckler` to `reports =`.

Add a CODEOWNERS to your repo.

Install and Authorize your app by going to https://github.com/settings/apps/heckler-dev and clicking "public page", which I think is also https://github.com/apps/heckler-dev.  Choose "Only select repositories" and select your puppet repo.

That sends you to your heckler instance with a code and installation ID.

You then copy that installation ID into hecklerd_conf.yaml
