## How to fork

You will want to fork this repo and the Debian repo-repo next to it.

Be sure that the repo-repo has had `git lfs install; git lfs track "*.deb"` run.

The GitHub actions in this repo use a few secrets that each add features.

### To push to dockerhub.io

 * `DOCKER_IO_TOKEN` - generated at dockerhub.io

### To debug failing actions interactively

 * `NGROK_TOKEN` - generated at ngrok
 * `USER_PASS` - the password you log into the worker with

### To push to a Debian repo-repo

 * `GPG_KEY` - generate a gpg signing key and put the secret key here
      ```bash
      export EMAIL=heckler@mason.ch
      export GNUPGHOME="$(mktemp -d)"; gpg --batch --generate-key <<EOF
      %echo Generating repo signing key
      %no-protection
      Key-Type: default
      Key-Length: 4096
      Subkey-Type: default
      Name-Real: Heckler Autosigning Key
      Name-Email: ${EMAIL}
      Expire-Date: 10y
      %commit
      %echo Done!
      EOF
      gpg --armor --export-secret-keys "${EMAIL}" > my-private-key.asc
      gpg --export "${EMAIL}" >! path/to/heckler-deb/docs/KEY.gpg
      ```
      
      Don't forget to save the public key to your repo or somewhere you distribute the documentation for this all! (`gpg --armor --export "${EMAIL}" > /path/to/repo-repo/docs/KEY.gpg`)

 <!-- * `GPG_EMAIL` - the email associated with the GPG_KEY (not secret, but convenient) -->
 * `REPO_DEPLOY_KEY` - a GitHub deploy key allowed to push to the specific GitHub repo that stores the Debian repo (Check "Allow write access").
  * `ssh-keygen -t rsa -b 4096 -f github_heckler-deb_deploy`, copy the private key to hecker, the public key to a deploy key on heckler-deb.
 <!-- * `REPO_NAME` - the name of the specific GitHub repo that stores the Debian repo-repo (not secret) -->
