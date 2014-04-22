# Local Quip Backup

Simple command-line script that generates a directory with a snapshot of your Quip account, based on what data can be exported via the API. Documents are represented as HTML.

## Running

```
./main.py --access_token="..." --output_directory=/path/to/dir
```

You can obtain a personal access token via [quip.com/api/personal-token](https://quip.com/api/personal-token). The output directory will be created if it does not exist already. If you wish to target an alternate Quip server, you can use the `--quip_api_base_url` flag.

## Caveats

The following items are not currently backed up:

* Messages in conversations
* Attachments to conversations
* Images in documents
* Contacts

You may run into rate limitting issues depending on the size of your account.

Resuming of interrupted backups is currently not supported.
