## Welcome to atomburg

阿特博格

You can use the [editor on GitHub](https://github.com/atomburg/atomburg.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```javascript
var WebSocketServer = require('ws').Server; var Net = require('net'); var wss = new WebSocketServer({port: 8181}); var upstream = Net.connect({host: '10.59.97.214', port: 6379}, function(){ console.log('Ok, connected to server'); }); var conn = null; wss.on('connection', function (_conn){ console.log('client connected'); conn = _conn; conn.on('message', function (message){ console.log('[WS-R], received data'); console.log(message); console.log('[WS-T], forward to upstream'); upstream.write(message); }); }); upstream.on('data', function(data){ console.log('[US-R], received data'); console.log(data.toString()); console.log('[US-T], response to downstream'); conn.send(data); }); upstream.on('end', function(){ console.log('Ok, close connection'); });
[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/atomburg/atomburg.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
