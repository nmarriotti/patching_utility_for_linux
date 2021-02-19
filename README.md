# Linux Patching Utility

This script creates a snapshot of files and/or entire directory structures and patches files that are specified in a manifest file. Patching is completed using the diff and patch commands.

## How to Use

Open _manifest.cfg_ and add each file or folder that you would like included in the patch to a new line.
__NOTE:__ The manifest.cfg file should contain an empty line at the end of the file.

### Build the Manifest

The manifest contains MD5 hashes, file paths for where the file/folder resides in the patch, and the destination where the file/folder is to be placed on the fileystem as well as the file attributes.

```
./patch build
```

### Patching

If a file needs to be patched, a backup of the original file is taken and stored in the backup/ directory

```
./patch
```

### Restore

MD5 hashes of the backed up file and the currently deployed file are compared. If there are discrepancies then the file will be restored from the backup.

```
./patch restore
```
