# whatsapp-cli

Command line interface of whatsapp web in the terminal (Unofficial). </br>
This works with selenium-webdriver to login to whatsapp web interface and search the reciever name.

### Features

  - Send and receive messages to and from any contact/group in your WhatsApp *from command line*.
  - Switch between different chats *from command line*.

## Requirements

- [Python 3](https://www.python.org/downloads) Tested with 3.4.3, 3.6.1. **Python 2 will not work**
- [selenium](http://selenium-python.readthedocs.io/installation.html) Tested with 2.53.6, 3.4.2
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) Tested with 2.24, 2.29
- [Chrome Web Browser](https://www.google.com/chrome/browser/desktop) compatible with the ChromeDriver version you downloaded. (Eg. ChromeDriver 2.29 supports Chrome v56-58) You can get this info from the ChromeDriver download page.

## Installation

1.  Clone this repository. `$ git clone https://github.com/sspeedy/whatsapp-cli.git` 
2.  Install virtualenv `$ sudo pip3 install virtualenv`
3.  Create the virtual environment `$ virtualenv whatsapp`
4.  Activate the virtual environment `$ source whatsapp/bin/activate`
5.  Install selenium. `$ sudo pip3 install selenium`
6.  Download and extract [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/downloads).zip
7.  Put path to ChromeDriver executable in the line `'chromedriver_path': '/path/to/chromedriver'` in `chat.py` file of this repository.

## Related Repository
In order to not reinvent the wheel, some of the stuff and generic ideas are taken from here. </br>
[WhatsApp Bot](https://github.com/harshirtsidhwa/WhatsApp-bot-selenium)

## Usage

#### Start Chatting  

`$ python chat.py <name>`
  
1.  Replace `<name>` with the name of a contact or a group in your WhatsApp. Even partial names will work.
2.  Scan the QR code displayed on screen from the WhatsApp mobile app.
3.  Press `y` in console after WhatsApp Web is done loading, to connect your phone.


#### Stop sending messages and only receive messages

`stopsending`

1.  Type it while `chat.py` is running.
1.  This will allow you to only see incoming messages. Your messages won't be sent. To send messages again, restart the script.

#### Configuration

In `chat.py` file:

```
config = {
    'chromedriver_path': '/path/to/chromedriver',
    'get_msg_interval': 5,  # Time (seconds). Recommended value: 5
    'colors': True,  # True/False. True prints colorful msgs in console
    ...
}
```

#### Exit

Press `Ctrl+C` two times.

### Updates
To add Recent chats option. </br>
Ability to see all the unread messages </br>
Automate the activate using shell scripts </br>



### License 

[MIT](https://choosealicense.com/licenses/mit/)
