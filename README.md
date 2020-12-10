The source code for http://bluemix.github.io. Statically generated using [Hexo](http://hexo.io).


## How to deploy to bluemix.github.io
1) `hexo clean` (to fix the issue of having duplicate article title on the blog home page)
2) `hexo generate`
3) `git add .`
4) `git comit -m <message>`
5) add the same message for deployment reason:
   `vim _config.yaml`
6) `git push`
7) `hexo deploy`
