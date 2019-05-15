<html>
  <head>
    <meta charset="UTF-8">
    <title>Himanshu Mittal's space on the Interwebs</title>
  </head>
  <body>
    
## Here's a list of posts on this website.
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
  </body>
</html>
