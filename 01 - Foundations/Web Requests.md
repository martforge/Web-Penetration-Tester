# Web Requests

## Concepts
[HTTP](https://tools.ietf.org/html/rfc2616) is an application-level protocol used to access the World Wide Web resources.
Port 80


Let's look at the structure of a URL
![[Pasted image 20261004171920.png]]
|**Component**|**Example**|**Description**|
|---|---|---|
|`Scheme`|`http://` `https://`|This is used to identify the protocol being accessed by the client, and ends with a colon and a double slash (`://`)|

|`User Info`|`admin:password@`|This is an optional component that contains the credentials (separated by a colon `:`) used to authenticate to the host, and is separated from the host with an at sign (`@`)|

|`Host`|`inlanefreight.com`|The host signifies the resource location. This can be a hostname or an IP address|

|`Port`|`:80`|The `Port` is separated from the `Host` by a colon (`:`). If no port is specified, `http` schemes default to port `80` and `https` default to port `443`|

|`Path`|`/dashboard.php`|This points to the resource being accessed, which can be a file or a folder. If there is no path specified, the server returns the default index (e.g. `index.html`).|

|`Query String`|`?login=true`|The query string starts with a question mark (`?`), and consists of a parameter (e.g. `login`) and a value (e.g. `true`). Multiple parameters can be separated by an ampersand (`&`).|

|`Fragments`|`#status`|Fragments are processed by the browsers on the client-side to locate sections within the primary resource (e.g. a header or section on the page).|

![[Pasted image 20261005154331.png]]

[cURL](https://curl.haxx.se/) (client URL) is a command-line tool and library that primarily supports HTTP along with many other protocols.

-O to download a page or a file and output the content into a file
-s silent the status

Usage: curl [options...] <url> -d, --data <data> HTTP POST data -h, --help <category> Get help for commands -i, --include Include protocol response headers in the output -o, --output <file> Write to file instead of stdout -O, --remote-name Write output to a file named as the remote file -s, --silent Silent mode -u, --user <user:password> Server user and password -A, --user-agent <name> Send User-Agent <name> to server -v, --verbose Make the operation more talkative

## Tools & Commands

## Techniques

## Exercises

## My Mistakes

## Key Takeaways

# Web Requests

## HTTP

HTTP is an application-level protocol used for communication between a client and a web server.

Basic flow:

Client → HTTP Request → Server
Client ← HTTP Response ← Server

Default ports:
- HTTP → 80
- HTTPS → 443

## URL Structure

Example:

http://admin:password@inlanefreight.com:80/dashboard.php?login=true#status

- Scheme → http
- User Info → admin:password
- Host → inlanefreight.com
- Port → 80
- Path → /dashboard.php
- Query String → ?login=true
- Fragment → #status

## HTTP Flow

1. Browser resolves the domain through DNS.
2. DNS provides the IP address.
3. Browser sends an HTTP request to the server.
4. Server processes the request.
5. Server sends an HTTP response.
6. Browser renders the response.

## cURL

cURL is a command-line tool used to send HTTP requests and interact with web resources.

### Useful options

curl <URL>
→ Send a basic request

-O
→ Save using the remote filename

-o <filename>
→ Save using a specified filename

-s
→ Silent mode

-h
→ Show help

-v
→ Verbose output

## My Understanding

[write this after finishing the section]

## My Mistakes

[write this if I make any]

## Key Takeaways

[write 3-5 things I should remember]