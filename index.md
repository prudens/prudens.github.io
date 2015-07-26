---
layout: default
custom_css: true
---
<p><br /><b>我的文章</b></p>
  <ul class="posts">
    {% for post in site.posts %}
      <li class="list_item">
      <a href="{{ post.url }}">{{ post.title }}
      </a></li>
    {% endfor %}
  </ul>

<p><br /><b>我的项目</b></p>
<ul class="posts mylist">
  <li class="list_item"><a href="https://github.com/prudens">Github</a></li>
  <!--<li class="list_item"><a href="#">Book</a></li> -->
</ul>


