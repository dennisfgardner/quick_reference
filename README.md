# Quick Reference

Snippets I have useful.

## Terminal

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
