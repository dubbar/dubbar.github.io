---
layout: post
title: Dot product without numpy
<!-- date: '2015-08-18 15:07:19 -->'
categories:
  - python
comments: true
published: true
---
Using numpy it's simple task
Say we have two matrices or arrays a and b
Then dot product is 


~~~ python
import numpy as np
a=np.array([1,2,3])
b=np.array([4,5,6])
print(np.dot(a,b))
if 3>2:
  print('hi')
~~~ 
> 32 <br />

   
~~~ python
import numpy as np
def matrixmul(a,b):
    r1,c1=a.shape
    r2,c2=b.shape
    if c1!=r2:
        print('Rows of 1st matrix is not equal to columns of second matrix')
    else:
        l3=[]
        for k in range (r1):
            l2=[]
            for j in range (c2):
                l1=0
                for i in range (c1):
                    l1+=a[k,i]*b[i,j]
                l2.append(l1)
            l3.append(l2)
        print(l3)
    return 
    
a=np.matrix([[1,2,3],\
            [4,5,6]])
b=np.matrix([[1],[2],[3]])   
matrixmul(a,b)
~~~
> [[14], [32]]




<!-- You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works. -->

<!--more-->







Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT. and this is comment
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
