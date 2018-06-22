# Github-api

Github api demo

### 基础Api地址

https://api.github.com

直接点击打开，可看到当前所有可用接口。

- gitbook: https://legacy.gitbook.com/book/1030310877/github-api-v3/details
  - https://1030310877.gitbooks.io/github-api-v3/content/authenticate/Authorizations.html


## api

### GET /users/{username}

获取中指定用户信息，username指的是用户的登录名(login)

- https://api.github.com/users/fairyly

### 获取 followers 接口
- https://api.github.com/users/fairyly/followers

```
返回：
avatar_url:"https://avatars1.githubusercontent.com/u/7548209?v=4"
events_url:"https://api.github.com/users/smacheng/events{/privacy}"
followers_url:"https://api.github.com/users/smacheng/followers"
following_url:"https://api.github.com/users/smacheng/following{/other_user}"
gists_url:"https://api.github.com/users/smacheng/gists{/gist_id}"
gravatar_id:""
html_url:"https://github.com/smacheng"
id:7548209
login:"smacheng"
node_id:"MDQ6VXNlcjc1NDgyMDk="
organizations_url:"https://api.github.com/users/smacheng/orgs"
received_events_url:"https://api.github.com/users/smacheng/received_events"
repos_url:"https://api.github.com/users/smacheng/repos"
site_admin:false
starred_url:"https://api.github.com/users/smacheng/starred{/owner}{/repo}"
subscriptions_url:"https://api.github.com/users/smacheng/subscriptions"
type:"User"
url:"https://api.github.com/users/smacheng"
```





### 参考
- https://blog.csdn.net/qq_25537177/article/details/80561507
