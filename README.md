Clone the repo.

Get the password from a team member.

Inside the directory, run this command and enter the password:

`openssl aes-256-cbc -d -a -md sha512 -in config.enc -out config`

Then, you can update the `KUBECONFIG` environment variable in the OpenQ context on CircleCI by base64 encoding the outputted plaintext file

`base64 config`