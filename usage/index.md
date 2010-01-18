---
layout: default
title: Usage
---

# Usage

<hr id=toc>

1.  [Hello World](#hello-world)

<h2 id=hello-world>Hello World</h2>

<pre class=prettyprint><code>"""
hello world

"""

import web

resources = (
  r'/(.*)', 'Hello'
)
webapp = web.application(resources, globals())

class Hello:
  """
  say Hello
  
  """
  
  def GET(self, name):
    if not name: 
        name = 'World'
    return 'Hello ' + name + '!'

if __name__ == '__main__':
  webapp.run()</code></pre>

[ [download](/usage/hello.py?format=raw) ]

<script src=http://angelo.gladding.name/assets/jquery.js></script>
<script src=http://angelo.gladding.name/assets/js-prettify/prettify.js></script>
<script>$(document).ready(function() { prettyPrint(); });</script>
<style>
@import url(http://angelo.gladding.name/assets/js-prettify/prettify.css);
@import url(http://angelo.gladding.name/assets/webpy-redesign.css);
</style>