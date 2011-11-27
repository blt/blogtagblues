I'm using the [Middleman Blog](http://middlemanapp.com/guides/blog/) guide for reference material. 

```
$ gem install middleman
********************************************************************************

  Welcome to Middleman 2.0
  
  In addition to many new features, some backwards-incompatible
  changes have been made to the structure of Middleman sites.
  
  Before running you old, v1.x project on Middleman 2.0,
  review the Migration guide:
  
  http://middlemanapp.com/guides/migrating

********************************************************************************
Successfully installed middleman-2.0.14
1 gem installed

$ gem install middleman-blog
Successfully installed middleman-blog-0.1.3
1 gem installed

$ middleman init blogtagblues --template=blog                                  
/home/blt/.rvm/gems/ruby-1.9.3-p0/gems/middleman-2.0.14/lib/middleman/guard.rb:
5: Use RbConfig instead of obsolete and deprecated Config.
      create  blogtagblues/config.ru
      create  blogtagblues/config.rb
      create  blogtagblues/source
      create  blogtagblues/source/2011/01/01/new-article.html.markdown
      create  blogtagblues/source/_article_template.erb
      create  blogtagblues/source/archives/index.html.erb
      create  blogtagblues/source/feed.xml.builder
      create  blogtagblues/source/index.html.erb
      create  blogtagblues/source/layout.erb
      create  blogtagblues/source/stylesheets
      create  blogtagblues/source/javascripts
      create  blogtagblues/source/images
```

You may find blogtagblues [here](https://github.com/blt/blogtagblues). I edit `source/2011/01/01/new-article.html.markdown` to look like so:

```

--- 
title: "New Article title"
date: 01/01/2011
tags: blogging
---

Content of my article
```

and find that, after I've started up `middleman server` for this project I'm greeted with the exception:

```
NameError at /
undefined local variable or method `blog_taglink' for #<#<Class:0x9c948bc>:0xaef6a64>
file: feature.rb location: block (3 levels) in registered line: 96
```

