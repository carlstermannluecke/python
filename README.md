## lesson12
so let's consider this class

## Welcome to python website

You can find here the [our python code for ping pong](https://github.com/zainabnazari/python/blob/master/pingictp.ipynb) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

import numpy as np
from numpy.random import choice
def tour(b,r):
    c=b.size//2
    pair=choice(b, size=(c,2), replace=False)
    print("************************")
    print("This is the",r,"round")
    print(pair)
    if b.size % 2 ==1:
     notchosen=b[np.isin(b, pair)==False]
     print("Number", notchosen, "needs to wait.")
    winners=np.asarray(eval(input("Who (are) is the winner(s)? ")))
    if b.size %2==1:
     if winners.size>1:
       lucky=np.asarray(choice(winners, size=(notchosen.size)))
     else:
      lucky=winners
     print("Number", notchosen, "needs to play against", lucky)
     who=np.asarray(eval(input("Who won? ")))
     winners=np.asarray(np.where(winners==lucky, who, winners))
    return winners
p=input("Number of players: ")
a=eval(p)
r=1
people=np.arange(a)
while people.size>=2:
      people=np.asarray(tour(people,r))
      r=r+1
print("Cheers!")

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/zainabnazari/python/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
