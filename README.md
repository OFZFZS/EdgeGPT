<div align="center">
  <img src="https://socialify.git.ci/acheong08/EdgeGPT/image?font=Inter&language=1&logo=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F9%2F9c%2FBing_Fluent_Logo.svg&owner=1&pattern=Floating%20Cogs&theme=Auto" alt="EdgeGPT" width="640" height="320" />

  # Edge GPT

  *The reverse engineering the chat feature of the new version of Bing*

</div>

<p align="center">
  <a href="https://github.com/acheong08/EdgeGPT">
    <img alt="PyPI version" src="https://img.shields.io/pypi/v/EdgeGPT">
  </a>
  <img alt="Python version" src="https://img.shields.io/badge/python-3.7+-blue.svg">
</p>

#  

> ## UPDATE 2023/02/13 - Public access shut down by Microsoft
> ## UPDATE 2023/02/14 - Do not use for now while I verify its safety

## Table of Contents
- [Edge GPT](#edge-gpt)
- [](#)
  - [Table of Contents](#table-of-contents)
  - [Setup](#setup)
    - [Install package](#install-package)
    - [Requirements](#requirements)
    - [Checking access (Required)](#checking-access-required)
    - [Getting authentication (Required)](#getting-authentication-required)
  - [Usage](#usage)
    - [Quick start](#quick-start)
    - [Developer demo](#developer-demo)
  - [Work in progress](#work-in-progress)
  - [Contributors](#contributors)

## Setup

### Install package
```bash
python3 -m pip install EdgeGPT --upgrade
```
 
### Requirements 
We have a shared token for public use. If you have your own account with access, you can use that instead.
 
- python 3.7+
- Microsoft Edge (Required)
- A Microsoft Account with early access to http://bing.com/chat (Required)


<details>
  <summary>
 
  ### Checking access (Required)
 
  </summary>
 
- Install the latest version of Microsoft Edge
- Open http://bing.com/chat
- If you see a chat feature, you are good to go
 
</details>


<details>
  <summary>
 
  ### Getting authentication (Required)
 
  </summary>

- Open the developer tools (F12)
- Go to the Application tab → Storage → Cookies
- Find the cookie named "_U"
- Copy the value of the cookie
 
</details>



## Usage

### Quick start
 
```
 $ python3 -m EdgeGPT -h

        EdgeGPT - A demo of reverse engineering the Bing GPT chatbot
        Repo: github.com/acheong08/EdgeGPT
        By: Antonio Cheong

        !help for help

        Type !exit to exit
        Enter twice to send message

usage: EdgeGPT.py [-h] [--no-stream] [--bing-cookie BING_COOKIE]

options:
  -h, --help            show this help message and exit
  --no-stream
  --bing-cookie BING_COOKIE (Required)
```

-----

### Developer demo
Use Async for the best experience

[Reference code](https://github.com/acheong08/EdgeGPT/blob/master/src/EdgeGPT.py#L268-L328) for more advanced example of usage

```python
import asyncio
from EdgeGPT import Chatbot

async def main():
    bot = Chatbot()
    print(await bot.ask(prompt="Hello world"))
    await bot.close()


if __name__ == "__main__":
    asyncio.run(main())

```

## Work in progress
- Error handling

## Star History
[![Star History Chart](https://api.star-history.com/svg?repos=acheong08/EdgeGPT&type=Date)](https://star-history.com/#acheong08/EdgeGPT&Date)


## Contributors
This project exists thanks to all the people who contribute. 
- pig#8932 (Discord) - Sharing account with beta access
- ulysses115#7373 (Discord) - Sharing account with beta access
- [Jimmy-Z](https://github.com/Jimmy-Z) - Bugfixes
 <a href="https://github.com/acheong08/EdgeGPT/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=acheong08/EdgeGPT" />
 </a>
