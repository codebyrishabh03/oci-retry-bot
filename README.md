# oci-retry-bot

Our own script, not a third-party one. Retries creating an Always-Free Oracle
Ampere A1.Flex instance every 15 minutes via GitHub Actions until it succeeds,
then stops on its own (checks for an already-running instance first).

## Secrets (Settings -> Secrets and variables -> Actions -> Secrets)

- `OCI_USER_ID`
- `OCI_TENANCY_ID`
- `OCI_KEY_FINGERPRINT`
- `OCI_REGION`
- `OCI_PRIVATE_KEY` -- full contents of the API signing key .pem file, pasted as-is
- `OCI_SSH_PUBLIC_KEY` -- contents of the .pub file for the instance you want to SSH into

## Variables (same page, "Variables" tab -- not sensitive, plain text)

- `OCI_DISPLAY_NAME`
- `OCI_AVAILABILITY_DOMAIN`
- `OCI_SHAPE`
- `OCI_OCPUS`
- `OCI_MEMORY_IN_GBS`
- `OCI_SUBNET_ID`
- `OCI_IMAGE_ID`
- `OCI_BOOT_VOLUME_GBS`

## Manually trigger a run

Actions tab -> OCI ARM Catcher -> Run workflow.
