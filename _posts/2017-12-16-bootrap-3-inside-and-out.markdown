---
layout: post
title: Bootstrap 3 - Inside and Out
date: 2017-12-12 00:00:00 +0300
description: Bootstrap 3 Notes and Interview Questions # Add post description (optional)
img: how-to-start.jpg # Add image post (optional)
tags: [Bootstrap 3] # add tag
---


# Bootstrap-3 Inside and Out
Button  

```HTML
<button class="btn btn-default">Click ME</button>
```

Button Group
```HTML
<div class="btn-group btn-group-justified">
  <div class="btn-group">
    <button class="btn btn-success">Home</button>
  </div>
  <div class="btn-group">
    <button class="btn btn-success">About</button>
  </div>
  <div class="btn-group">
    <button class="btn btn-success">Contact</button>
  </div>
  <div class="btn-group">
    <button class="btn btn-success">FAQ</button>
  </div>
</div>
```

Dropdown
```HTML
<div class="dropdown">
  <button class="btn btn-primary dropdown-toggle" data-toggle="dropdown"> Article <span class="caret"></span></button>
  <ul class="dropdown-down">
    <li><a href="#">Tech</a></li>
    <li><a href="#">Mech</a></li>
    <li><a href="#">Cech</a></li>
    <li class="divider"></li>
    <li class="dropdown-header">Personal</li>
    <li><a href="#">Logout</a></li>
  </ul>

</div>
```

Glyphicon
```HTML
<span class="glyphicon glyphicon-camera"></span>
```
