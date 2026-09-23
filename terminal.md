
# Terminal Quick Reference

## Disk and Files

### Size of directory

```sh
du -sh <dir_path>
```

Use the *disk usage* command with the `-s` argument to summarize the results and `-h` give human-readable output.

### Largest files and subdirectories inside current directory

```sh
du -ahx . | sort -rh | head -n 10
```

The `-a` gets the size of all files and directories and the '-x' argument prevents `du` from going into other mounted/networked drives. The `-r` argument with the `sort` command reverses the results to the largest files are on top.

### Number of files in a directory

List the files and pipe them into word count.

```bash
ls /media/dennis/1TBdrive/zips/ | wc
```

### Unzip a bunch of files

This uses the `xargs` command, which lets you take the output of one command and use it as arguments to another.

The `-I {}` flag defines `{}` as a placeholder — for each line of input, xargs substitutes `{}` with that line and runs the given command. Below, `unzip` runs once per file listed by `ls`, with `{}` replaced by each filename.

The `-d` flag for `unzip` places the extracted files in the specified directory instead of the current one.

```bash
ls zips/ | xargs -I {} unzip zips/{} -d unzips/
```

> Note: this breaks on filenames with spaces.

## Working on Remote Machines

### Generate a Key

You only need to do this once.

```bash
ssh-keygen -t ed25519 -C "<comment>"
```

For the `<comment>`, I do an email or a computer description like "raspberry_pi".
The comment labels the keys online so you can manage them.

I use the default location and I typically don't use a passphrase (just leave blank and press Enter).
If you do use a passphrase, which is more secure, then you need to enter it in every time you push or pull.

### SSH w/o password

Copy the public key to the remote host so you don't need to enter a password every time you log in.
After putting the key on the host, you can just `ssh <username>@<IP_address>`

```bash
ssh-copy-id <username>@<IP_address>
```

You'll be asked for the remote's password to copy the key.

### Setting up SSH with online repositories

The step are similar for Github and Gitlab.

First you need to copy the public key.
This is system dependent.

#### MacOS

`pbcopy < ~/.ssh/id_ed25519.pub`

#### Linux

You might need to install xclip if you don't have it.

`xclip -sel clip < ~/.ssh/id_ed25519.pub`

#### Windows

`cat ~/.ssh/id_ed25519.pub | clip`

#### Text Editor

Alternatively, you can open the public key in a text editor and copy it.

#### Paste key online

Navigate to the SSH setting of the online host and paste in the public key.

You can test if it's successful with the following, for example:

`ssh -T git@github.com`

And yes, it should be git@ not my_username@git.

## PDFs

Here's a terminal command using ghostscript to reduce PDF file size:

`gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf`

Replace input.pdf and output.pdf with your actual filenames.

Quality settings (adjust -dPDFSETTINGS):
- /screen — lowest quality, smallest file (web viewing)
- /ebook — good compression with reasonable quality (recommended for most cases)
- /printer — higher quality, moderate compression
- /prepress — highest quality, minimal compression

For even smaller files at lower quality, try /screen instead of /ebook.