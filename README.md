# Drive Secrets

Don't store secrets in plaintext in Colaboratory notebooks. Instead, store them in your Google Drive.

## Quickstart

Add the following to your Colaboratory notebook.

```
!pip install drivesecrets

from drivesecrets import get_secret

# If your secret exists, get it as plaintext. If it doesn't, prompt you and save it.
api_key = get_secret("api_key.txt")
```

The first time that get_secret is called, you will be prompted for the secret you'd like to save. Input it and it will be saved (but delete the cell's output using, or else your input will be saved in the notebook.)

The second time it is called, it'll just be returned as plaintext.

If you make a mistake, delete this file from your Google drive and re-invoke the function.

## Important

The secret you save is now in plaintext in your Google Drive. Anyone with access to your Google Drive can read it as a text file.

## Troubleshooting

1. Help! I've input the wrong secret.

The argument to get_secret is the filename under which your secret is stored. Navigate to the root of your Google Drive and delete that file. You'll be prompted again.
