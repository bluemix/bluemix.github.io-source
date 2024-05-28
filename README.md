The source code for http://bluemix.github.io. Statically generated using [Hexo](http://hexo.io).


## How to deploy to bluemix.github.io
1) `hexo clean` (to fix the issue of having duplicate article title on the blog home page)
2) `hexo generate`
3) `git add .`
4) `git commit -m <message>`
5) add the same message for deployment reason:
   `vim _config.yaml`
5.1) `git add .`
6) `git commit -m 'updating _config.yaml commit message'`
7) `git push`
8) `hexo deploy`
