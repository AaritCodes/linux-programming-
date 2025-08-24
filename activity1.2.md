Activity-1: Basic Linux Commands (ls options)

---
## Command
\\`\\`\\`bash
ls -a
\\`\\`\\`
## Description
Lists all files including hidden ones (those starting with .).
## Output
.
..
activity1_2.md
activity.sh
.bash_logout
.bashrc
.cache
.config
Desktop
Documents
.dotnet
Downloads
.local
Music
Pictures
.pki
.profile
Public
snap
:
.ssh
.sudo_as_admin_successful
Templates
Videos
.vscode
## Remarks
Shows hidden files like .bashrc, and directories . (current) and .. (parent).

---
## Command
\\`\\`\\`bash
ls -b
\\`\\`\\`
## Description
Prints non-graphic characters in octal notation.
## Output
activity1_2.md
activity.sh
Desktop
Documents
Downloads
Music
Pictures
Public
snap
Templates
Videos
:
## Remarks
Useful for identifying spaces or special characters in filenames.

---
## Command
\\`\\`\\`bash
ls -c
\\`\\`\\`
## Description
Sorts files by ctime (last status change time).
## Output
activity1_2.md
snap
activity.sh
Downloads
Desktop
Documents
Music
Pictures
Public
Templates
Videos
## Remarks
Order depends on metadata change times.

---
## Command
\\`\\`\\`bash
ls -d */
\\`\\`\\`
## Description
Lists directories themselves, not their contents.
## Output
Desktop/
Documents/
Downloads/
Music/
Pictures/
Public/
snap/
Templates/
Videos/
## Remarks
Helps when you only want to see directory names.

---
## Command
ls -e
## Description
Not available in GNU ls on Ubuntu.
## Output
N/A
## Remarks
The -e option is supported on BSD/macOS but not in Ubuntu.
:

---
## Command
\\`\\`\\`bash
ls -f
\\`\\`\\`
## Description
Lists files without sorting.
## Output
.sudo_as_admin_successful
Documents
.profile
.config
.local
.bash_logout
Public
.dotnet
Templates
.vscode
.
.bashrc
Music
activity.sh
Downloads
Desktop
snap
Videos
activity1_2.md
.pki
..
:
..
.cache
Pictures
.ssh
## Remarks
Useful for quick listing when order doesn’t matter.

---
## Command
ls -z
## Description
Not available in GNU ls on Ubuntu.
## Output
N/A
## Remarks
The -z option is related to SELinux context and is not supported in Ubuntu's ls.

# Activity-2: Basic Linux Commands (tree options)

---
## Command
\\`\\`\\`bash
tree -a
\\`\\`\\`
## Description
Lists all files and directories including hidden ones.
## Output
.
:
## Output
.
├── activity1_2.md
├── activity.sh
├── .bash_logout
├── .bashrc
├── .cache  [error opening dir]
├── .config  [error opening dir]
├── Desktop
├── Documents
├── .dotnet  [error opening dir]
├── Downloads
│   ├── activity1_2.md
│   ├── activity.sh
│   └── code_1.103.2-1755709794_amd64.deb
├── .local  [error opening dir]
├── Music
├── Pictures
├── .pki  [error opening dir]
├── .profile
:
├── Public
## Remarks
Good for seeing hidden directory structures. (Showing first 20 lines for brevity)

---
## Command
\\`\\`\\`bash
tree -d
\\`\\`\\`
## Description
Shows only directories, not files.
## Output
.
├── Desktop
├── Documents
├── Downloads
├── Music
├── Pictures
├── Public
├── snap
│   ├── firefox  [error opening dir]
│   ├── snapd-desktop-integration  [error opening dir]
│   ├── snap-store  [error opening dir]
│   └── tree
│       ├── 54
│       ├── common
│       └── current -> 54
:
17 directories
## Remarks
Useful for focusing only on directory hierarchy.

---
## Command
\\`\\`\\`bash
tree -u
\\`\\`\\`
## Description
Displays file owner (user) for each entry.
## Output
[Aarit   ]  .
├── [Aarit   ]  activity1_2.md
├── [Aarit   ]  activity.sh
├── [Aarit   ]  Desktop
├── [Aarit   ]  Documents
├── [Aarit   ]  Downloads
│   ├── [Aarit   ]  activity1_2.md
│   ├── [Aarit   ]  activity.sh
│   └── [Aarit   ]  code_1.103.2-1755709794_amd64.deb
├── [Aarit   ]  Music
├── [Aarit   ]  Pictures
├── [Aarit   ]  Public├── [Aarit   ]  snap
│   ├── [Aarit   ]  firefox  [error opening dir]
│   ├── [Aarit   ]  snapd-desktop-integration  [error opening dir]
│   ├── [Aarit   ]  snap-store  [error opening dir]
│   └── [Aarit   ]  tree
│       ├── [Aarit   ]  54
│       ├── [Aarit   ]  common
│       │   └── [Aarit   ]  marker_publisher_changed_announcement_shown
## Remarks
Shows which user owns which files (showing first 20 lines).

---
## Command
\\`\\`\\`bash
tree -p
\\`\\`\\`
## Description
Displays file permissions.
## Output
[drwxr-x---]  .
├── [-rw-rw-r--]  activity1_2.md
├── [-rwxrwxr-x]  activity.sh
├── [drwxr-xr-x]  Desktop
├── [drwxr-xr-x]  Documents
├── [drwxr-xr-x]  Downloads
│   ├── [-rw-rw-r--]  activity1_2.md
│   ├── [-rw-rw-r--]  activity.sh
│   └── [-rw-rw-r--]  code_1.103.2-1755709794_amd64.deb
├── [drwxr-xr-x]  Music
├── [drwxr-xr-x]  Pictures
├── [drwxr-xr-x]  Public
├── [drwx------]  snap
│   ├── [drwxr-xr-x]  firefox  [error opening dir]
│   ├── [drwxr-xr-x]  snapd-desktop-integration  [error opening dir]
│   ├── [drwxr-xr-x]  snap-store  [error opening dir]
│   └── [drwxr-xr-x]  tree
│       ├── [drwxr-xr-x]  54
│       ├── [drwxr-xr-x]  common
│       │   └── [-rw-rw-r--]  marker_publisher_changed_announcement_shown
## Remarks
Useful for analyzing permission structures (showing first 20 lines).





