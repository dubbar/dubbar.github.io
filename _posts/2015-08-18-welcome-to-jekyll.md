---
layout: post
title: Dot product without numpy
<!-- date: '2015-08-18 15:07:19 -->'
categories:
  - python
comments: true
published: true
---
Todo dot product using numpy is simple task, 
whereas if you desire to do without using numpy just follow the proceeding code 

<!--more-->

Using numpy it's simple task
Say we have two matrices or arrays a and b
Then dot product is 


~~~ python
import numpy as np
a=np.matrix([[1,2,3],\
            [4,5,6]])
b=np.matrix([[1],[2],[3]]) 
print(np.dot(a,b))

~~~ 
[[14]
 [32]]
{: .notice}

 

   
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
{: .notice}


Happy pythoning!
