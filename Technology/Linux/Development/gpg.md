## Creating an gpg key

1. Install gpg on your system
2. `gpg --full-generate-key`
3. Follow the instructions

## Creating a backup of a private gpg key
According to [JWilliker's post](https://www.jwillikers.com/backup-and-restore-a-gpg-key), these are the steps to creating a backup of your private gpg key:

### Exporting

1. Find the desired key with `gpg --list-secret-keys --keyid-format LONG`
2. Export it `gpg -o private.gpg --export-options backup --export-secret-keys <yourkeyhere>`. Replace `<yourkeyhere>` with your key's ID without the angled brackets.

The backup should now exist as `private.gpg`.

### Importing

1. Import the key `gpg --import-options restore --import private.gpg`.
2. If needed, you can change the key's level of trust with `gpg --edit-key <yourkeyhere>`, `trust`, select your level of trust, then `save` it.
