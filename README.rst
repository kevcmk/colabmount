# Drive Secrets

Don't store secrets in plaintext in Colaboratory notebooks. Instead, store them in your Google Drive. Anyone who has access to your Google Drive has access to the file.

## Quickstart

```
    !pip install drivesecrets

    from drivesecrets import get_secret

    # If your secret exists, get it as plaintext. If it doesn't prompt you and save it.
    openai_key = get_secret("openai_key.txt")
```

The first time that get_secret is called, you will be prompted for the secret you'd like to save. Input it and it will be saved.

If you make a mistake, delete this file from your Google drive and re-invoke the function.

## Important

The secret you save is now in plaintext in your Google Drive. Anyone with access to your Google Drive can read it as a text file.
