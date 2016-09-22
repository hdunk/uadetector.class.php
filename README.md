# uadetector.class.php
UADetector PHP class

A PHP4+ class for fast, accurate user agent detection.

version: 0.9.2

author: helened

Author URI: [http://helenesit.com](http://helenesit.com)

Copyright (c) 2009-2016 Helene Duncker

### Usage:
for detection of current user agent:
```
  include_once(uadetector.class.php);
  $ua_obj = new UADetector();
```

<dl><dt>$ua_obj has 16 fields:</dt>
<dd>  $ua_obj->name,</dd>
<dd>  $ua_obj->version,</dd>
<dd>  $ua_obj->os,</dd>
<dd>  $ua_obj->platform,</dd>
<dd>  $ua_obj->emulation,</dd>
<dd>  ...</dd>
<dd>  $ua_obj->agenttype (
      B=Browser, 
			F=feedreader (could also have type=R) 
			R=robot (spider|archiver|validator), 
			S=Spam/malware code in agent string
			)</dd>
<dd>  ...</dd>
</dl>
### Notes:
* UADetector attempts to find the actual browser in use. This may cause the "name" field to differ from "emulation" field when user-agent spoofing is detected. You should use the most appropriate field for your application type:
<ul><li>"Name" field is best for statistics collection</li>
<li>"Emulation" field is best for UI customizations by browser.</li>
</ul>
* UADetector was originally developed as a module for Wassup Wordpress plugin, a website analytics tool.


### Changelog:
  v0.9.2: updated for detection of Microsoft Edge browser on Windows and Windows Phone
