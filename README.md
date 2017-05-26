# aws-list

This script enumerates all AWS resources across all zones and prints details.
Useful for you to check you don't have something lurking in your account
that you'd forgotten about.

You'll need to create yourself a skew config file e.g. `~/.skew`, something like this:

```
---
  accounts:
    "<accountid>":
      profile: default
```

where `<accountid>` is the numeric account ID that you can find from your "My Account"
page in the AWS web console.

You'll also need an AWS credentials file `~/.aws/credentials` something like this:

```
[default]
aws_access_key_id = <accesskey>
aws_secret_access_key = <secret>
region = <region>
```

**NB:** Credit for this script goes to [Micheal Holtby](https://stackoverflow.com/users/6416315/michael-holtby)
for [his stack overflow](https://stackoverflow.com/a/37599862)
answer.  I just wanted to be able to find it again easily.