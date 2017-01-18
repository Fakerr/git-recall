# log-so-handy
> A convenient tool to easily go through your git logs.


![git hlog](http://imgur.com/bq9kRez.gif)

## Usage

```sh
$ git hlog   [-a <author name>] 
             [-d <days-ago>]
             [-f]
             [-h]
```

##### Options description:

- `-a`      - Restrict search for a specific user (use -a "all" for all users)
- `-d`      - Display commits for the last n days
- `-f`      - Fetch the latest changes
- `-h`      - Show help screen

##### How to use:

Once the commits are displayed, you can use the `arrow keys` or `j/k` to switch between commits,
press `TAB` to `expand/reduce` the commit's diff or `q` to quit.

##### Limitaions:

when the number of lines between the commits list and a commit's diff is higher than the number of lines of the current terminal session,
the result will be displayed using the [`less`](http://www.tutorialspoint.com/unix_commands/less.htm) program which will open the diff in a separate screen.
You can still use either `TAB` or `q` to return to the commits list.

## Examples

```sh
$ git hlog
# By default (without options), the command will display commits from yesterday and
# for the current user.
```


```sh
$ git hlog -d 5 -a "Doge"
# The command will show all Doge's commits from 5 days ago.

$ git hlog -d 5 -a "all"
# The command will show commits of all contributors from 5 days ago.
```


```sh
$ git hlog -f
# Fetch commits beforehand.
```

## Installation

##### Without using tools

```
You can install it by simply copying the `git-hlog` script into any existing path
(e.g. /usr/local/bin) or create your own directory and add it to the 'PATH' variable.
```

##### Using NPM
Use `npm` to install the project.

```sh
npm install --global log-so-handy
```
##### Manual install
Clone the project and install it using make install.

```sh
$ git clone https://github.com/Fakerr/log-so-handy.git
$ cd log-so-handy
$ sudo make install
```
## Requirements
- Linux or OSX

## Contribution
Pull requests are welcome, along with any feedback or ideas.


## License

MIT
