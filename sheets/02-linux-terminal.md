# Linux and terminal

Security tools live on the command line. You do not need to be a Linux expert,
but you need fluency in a core set of commands. This is that set.

## Navigation and files

| Command | Does |
| --- | --- |
| `pwd` | Where am I |
| `ls -la` | List everything, including hidden, with detail |
| `cd` | Move around |
| `cat` / `less` | Read a file (whole / paged) |
| `find / -name X` | Locate files by name |
| `cp` / `mv` / `rm` | Copy / move / delete |
| `chmod` / `chown` | Change permissions / ownership |

## Finding things inside files

| Command | Does |
| --- | --- |
| `grep pattern file` | Find lines matching a pattern |
| `grep -r pattern dir` | Search a whole directory tree |
| `wc -l` | Count lines |
| `sort` / `uniq` | Order / deduplicate |
| `head` / `tail` | First / last lines; `tail -f` follows a live file |

## Pipes and redirection, the real power

The Unix idea: small tools joined together. `|` sends one command's output into
the next; `>` writes output to a file; `>>` appends.

```
cat access.log | grep "404" | sort | uniq -c | sort -rn | head
```

That one line finds the most common missing pages in a web log. Chaining simple
tools like this is most of practical command-line work.

## System and network

| Command | Does |
| --- | --- |
| `ps aux` / `top` | What is running |
| `whoami` / `id` | Who am I, what can I do |
| `ip a` | Network interfaces and addresses |
| `ss -tulpn` | What ports are listening locally |
| `sudo` | Run as administrator (with care) |
| `man <cmd>` | The manual: your first stop, always |

## Permissions, the concept that trips people up

Every file has permissions for its owner, its group, and everyone else, each
some combination of read, write and execute. `ls -l` shows them as a string
like `-rwxr-xr--`. Understanding this is essential, because misconfigured
permissions are a whole category of security finding: a file everyone can write,
a script everyone can run, a secret everyone can read.

## Staying oriented

- `man <command>` and `<command> --help` answer most questions faster than a
  search.
- Keep notes of commands that worked. Your own annotated list beats any generic
  one.
- Practise in the lab until these are muscle memory. Fluency here is what makes
  everything else feel less like magic.
