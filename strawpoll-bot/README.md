# Strawpoll Bot

![](https://img.shields.io/badge/license-GPLv2-blue)

## Requirements:
- Python 2 or 3
- `pip install requests`

## Script Arguments:
- **id:** The strawpoll.me Poll ID
- **option:** Which option should the bots vote for? 1 for first checkbox, 2 for second, etc ...
- **f F:** Change the frequency of the votes (one every F ms)
- **m M:** Max M threads
- **p:** Use proxies (in case the poll is doing an IP Check)

![](/img/help.png)

## Limitations:
- It cannot vote for multiple options at once
- It cannot vote for polls with a captcha

## Demo:
![](/img/demo.png)


python3 script.py ceear16e 5 p -f 


id = ceear16e
option = 6


python3 script.py ceear16e 5

python3 script.py 13371337 1


parser =  argparse.ArgumentParser (description = "Example: python3 script.py 13371337 1")
parser.add_argument ("id", help = "strawpoll.me poll ID")
parser.add_argument ("option", help = "Poll checkbox number (1 for 1st option, 2 for 2nd, ...)")

parser.add_argument ("-f", help = "Voting frequency (in ms) (Default: 200ms)")
parser.add_argument ("-m", help = "Max threads (Default: 16)")
parser.add_argument ("-p", action='store_true', help = "Use proxies (if the poll is doing an IP Check) - WARNING: Slow!")