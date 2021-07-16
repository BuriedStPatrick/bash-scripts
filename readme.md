# bash-scripts

Just a bunch of scripts, aliases, and run-commands that I find useful. `.*rc`-files can be sourced in your shell profile. I have split them into different folders according to the shell I use.

## Git

To use this, you need the .gitrc. Either clone it or just download it directly. After which you source it:

```bash
# Download .gitrc
wget -O ~/.gitrc https://raw.githubusercontent.com/BuriedStPatrick/bash-scripts/main/zsh/.gitrc

# Source the script (might want to add this to your profile though)
source ~/.gitrc
```

These are in complete random order, very sorry about that. They are also *very* opinionated. I mostly use git whenever I'm in a terminal, and I really don't like typing, which upon further inspection, is probably not great when you're a software developer.

### Delete branch

Quickly delete a branch with:

```bash
db <branchname>
```

If a remote version exists, you'll be prompted to delete that as well if you want.

### Create branch

Quickly create a branch with:

```bash
cb <branchname>
```

You'll also be prompted to push that branch to the default remote (most likely origin).

### Rebase

Nice and fast rebase with:

```bash
rb <branchname>
```

### Push

So many characters when all you need is `p`.

```bash
# Standard 'git push'
p

# Force push... with lease! This ain't the wild west no more.
pf
```

### Pull

Okay, I'm really pushing the character limit here with TWO entire characters. Uses the --rebase flag because it should be the default.

```bash
pl
```

### Status

Quickly get the gist of your repo.

```bash
st
```

### Commit

No time to review changes when there's MORE CODE TO WRITE.

```bash
# "Commit and push": Stage all dirty files, commit them and push
cap "My commit message"

# "Commit all": Stage all dirty files, commit them, but don't push just yet
ca "My commit message"

# "Commit": Commit what you have already staged. So considerate.
c "My commit message"
```

### Merge

Never again accidentally create merge commits. In this house we only fast forward! Adds --ff-only flag to stop you from making a huge mistake.

```bash
m <branchname>
```

### Git tree

Lil' function to show the current git tree in an interactive scrollable list.

```bash
gt
```

