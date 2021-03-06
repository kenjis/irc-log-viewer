# PHP IRC Log Viewer

This is a general purpose IRC log viewer.
Feel free to fork and make changes.  
Pull requests will be handled promptly.

Be sure and name your eggdrop log files according to the prescribed format:
* {channel}.log.{yyyy}-{mm}-{dd} (Original sample log format)
* {yyyy}.{mm}.{dd}.txt (Tiarra log format)

Sample Apache VHost:

<VirtualHost *:80>
    ServerName rest.local
    
    DocumentRoot /var/www/irc-log-viewer/dev
    <Directory /var/www/irc-log-viewer/dev>
        AllowOverride All
    </Directory>
    
    SetEnv APP_CHANNEL rest
    SetEnv APP_NETWORK irc.freenode.net
    SetEnv APP_LOGDIR  /var/www/irc-log-viewer/dev/sample-logs
</VirtualHost>

Wish List:
* Highlight search string in HTTP_REFERER for users coming from Google search.
* Add shift-click to line selection
* Strip invalid unicode characters
* Linkify user names? (where to link to?)
