# Node JS empty site
[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

# Set node secondly
web.config
```
<rule name="Node JS MAIN">
    <match url="/io/?.*" />
    <action type="Rewrite" url="server.js" />
</rule>
```

# Set node more server
web.config
```
<handlers>
    <add name="server1" path="server1.js" verb="*" modules="iisnode" />
    <add name="server2" path="server2.js" verb="*" modules="iisnode" />
</handlers>
```
and
```
<rule name="Node JS MAIN">
    <match url="/io1/?.*" />
    <action type="Rewrite" url="server1.js" />
</rule>
<rule name="Node JS MAIN1">
    <match url="/io2/?.*" />
    <action type="Rewrite" url="server2.js" />
</rule>
```