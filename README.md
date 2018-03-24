# git-recall

> Simple and handy tool to easily recall what you've done

![git recall](http://imgur.com/zuw2LqW.gif)

## Purpose

`git-recall` is a simple tool that allows you to easily go through your commits and
check what you or other contributors in your team did. It doesn't aim to be a replacement for the
`git log` command, but just to be a convenient way to recall what you've done from your terminal.


## Usage

```sh
$ git recall   [-a <author name>]
               [-d <days-ago>]
               [-b <branch name>]
               [-p <paths>]
               [-f]
               [-h]
               [-v]
```

##### Options description:

- `-a`      - Restrict search for a specific user (use -a "all" for all users)
- `-d`      - Display commits for the last n days
- `-b`      - Specify branch to display commits from
- `-p`      - Specify path/s or file/s to display commits from
- `-f`      - Fetch the latest changes
- `-h`      - Show help screen
- `-v`      - Show version

##### How to use:

Once the commits are displayed, you can use either the `arrow keys` or `j/k` to switch between commits,
press `TAB` or `e` to `expand/reduce` the commit's diff or `q` to quit.

##### Limitations:

when the number of lines between the commits list and a commit's diff is higher than the current terminal session's number of lines,
the result will be displayed using the [`less`](http://www.tutorialspoint.com/unix_commands/less.htm) program which will open the diff in a separate screen.
You can still use either `TAB` or `q` to return to the commits list.

## Examples

```sh
$ git recall
# By default (without options), the command will display commits from yesterday and
# for the current user.
```


```sh
$ git recall -d 5 -a "Doge"
# The command will show all Doge's commits from 5 days ago.

$ git recall -d 5 -a "all"
# The command will show commits of all contributors from 5 days ago.
```


```sh
$ git recall -f
# Fetch commits beforehand.
```

## Installation

##### Without using tools

You can install it by simply copying the `git-recall` script into any existing path
(e.g. `/usr/local/bin`) or create your own directory and add it to the `PATH` variable.

Make sure to run `chmod +x /usr/local/bin/git-recall` or the directory in which you copied it to. 

##### Using NPM
Use `npm` to install the project.

```sh
npm install --global git-recall
```
##### Manual install
Clone the project and install it using make install.

```sh
$ git clone https://github.com/Fakerr/git-recall.git
$ cd git-recall
$ sudo make install
```
## Requirements
- OS: Linux or OSX
- Bash 4.3 or more
- Tools: git, less, sed

##### Optional Requirements
- For a better UX, it's recommended to have installed the `lesskey` program.

## Contribution
Pull requests are welcome, along with any feedback or ideas.


## License

MIT
