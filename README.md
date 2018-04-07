# Project 7 - WordPress Pentesting

Time spent: **15.5** hours spent in total

> Objective: Find, analyze, recreate, and document five vulnerabilities affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: User Enumeration 
  - [ ] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.0
    - Fixed in version: 4.2.4
  - [ ] GIF Walkthrough: <iframe src="https://giphy.com/embed/3JXIYARKt5VrHptAK9" width="479" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/3JXIYARKt5VrHptAK9">via GIPHY</a></p>
  - [ ] Steps to recreate: Go to the WordPress site and attempt to log in as any user with any password. You will be denied access. If you then attempt to enter using admin as username and anything as password, the user is notified that the incorrect password is used for an accpeted user. This allows for a brute force attack to gain entry by allowing an intuder to figure out a list of valid names.
  - [ ] Affected source code:
    - [Link 1](https://www.wpwhitesecurity.com/wordpress-security/wordpress-username-disclosure-vulnerability/)
2. (Required) Vulnerability Name or ID: Unauthorized Cross Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.4
  - [ ] GIF Walkthrough: <iframe src="https://giphy.com/embed/1pAkfGfmZM9YcXT7Hc" width="480" height="373" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/1pAkfGfmZM9YcXT7Hc">via GIPHY</a></p>
  - [ ] Steps to recreate: Obtain a png file that is sized greater than allowed to be uploaded on WordPress.
  Rename this file with a suitable XSS attack and uload the file under add new media. If a Wordpress admin then attempts to load this media file it will allow for a cross site scripting attack.
  - [ ] Affected source code:
    - [Link 2](https://www.rapid7.com/db/vulnerabilities/wordpress-cve-2017-9061)
3. (Required) Vulnerability Name or ID: Authenticated Stored Cross Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version:4.0
    - Fixed in version:4.6.1 
  - [ ] GIF Walkthrough: <iframe src="https://giphy.com/embed/3Bktf0ODPM0zaNmAST" width="480" height="415" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/3Bktf0ODPM0zaNmAST">via GIPHY</a></p>
  - [ ] Steps to recreate: As a user go to WordPress site and create a new page with  a post as follows "<a href=" [caption code=">]</a><a title=" onmouseover=alert('Hola') ">link</a>. This will allow the user to possibly obtain privilege escalation when users in higher tiers such as admins view the page and click the link.
  - [ ] Affected source code:
    - [Link 3](https://www.rapid7.com/db/vulnerabilities/wordpress-cve-2016-7168)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.# Web-Security Week-7
