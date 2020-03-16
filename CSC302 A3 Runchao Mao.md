# CSC302 A3 Runchao Mao
<font size=4>Bugzilla link: https://bugzilla.mozilla.org/show_bug.cgi?id=1366376</font>
## Diagnosis of the bug
<font size=4> The bug comes when browser have network error, bug just giving a simple error message is confusing the user, because they have no basic understanding of this bug. Solving this bug will give user a better understanding about what they are encountering</font>
## Propose a solution
<font size=4>A new line of message "**After backing to good network, see what happend: here**" message to the network error page such that user knows what happened.</font>
## Testing
- <font size=4>**malformedURI** error: No good way to test this</font>
- <font size=4>**dnsNotfound** error: Open mozilla firefox with no internet connection and enter any website will triger this error and modified page will be loaded. The network with high packet loss will triger this as well.</font>
- <font size=4>**nettimeout** error: Visit 10.255.255.1 to trigger this</font>
- <font size=4>**netReset** error: This is network reset by peer, please run the python3 file server.py in the repo and visit localhost:5500 to triger this error</font>
- <font size=4>**netOffline** error: this is trigger by the case that user wants to visit a website not in browser cache in offline mode. To switch to offline mode of mozilla firefox, please open it, right click on a blank tab area, tick "Menu Bar", On the tool bar shows up, click "File", tick "Work Offline". Visit a page that you never use this browser visited. Or clean the broswer cache and visit any website to trigger this error.</font>
- <font size=4>**sslv3Used** error: Failed to find a test case</font>
- <font size=4>**nssFailure2** error: visit uc.nsksystem.co.jp to trigger this error</font>
- <font size=4>**remoteXUL** error: This has been abandoned by mozilla firefox, but still have some legacy code. Just mentioned this. See: https://developer.mozilla.org/en-US/docs/Archive/Mozilla/Remote_XUL</font>
