# Github-api

## 创建 auth token
```
登录 GitHub 到设置--》 Developer settings---》Personal access tokens
created a token in Github -> Settings -> Personal access tokens -> Generate new token and chose only repo scope.
```

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
```
{
  "login": "fairyly",
  "id": 17672815,
  "node_id": "MDQ6VXNlcjE3NjcyODE1",
  "avatar_url": "https://avatars1.githubusercontent.com/u/17672815?v=4",
  "gravatar_id": "",
  "url": "https://api.github.com/users/fairyly",
  "html_url": "https://github.com/fairyly",
  "followers_url": "https://api.github.com/users/fairyly/followers",
  "following_url": "https://api.github.com/users/fairyly/following{/other_user}",
  "gists_url": "https://api.github.com/users/fairyly/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/fairyly/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/fairyly/subscriptions",
  "organizations_url": "https://api.github.com/users/fairyly/orgs",
  "repos_url": "https://api.github.com/users/fairyly/repos",
  "events_url": "https://api.github.com/users/fairyly/events{/privacy}",
  "received_events_url": "https://api.github.com/users/fairyly/received_events",
  "type": "User",
  "site_admin": false,
  "name": "fairy",
  "company": "damo",
  "blog": "https://fairyly.github.io/myblog",
  "location": "hangzhou",
  "email": null,
  "hireable": null,
  "bio": ":fist: :octocat: :cn:  I don't like you, just because I didn't work hard enough！！:rose: :biking_man:  :biking_man: :biking_man: :biking_man:",
  "public_repos": 519,
  "public_gists": 1,
  "followers": 23,
  "following": 124,
  "created_at": "2016-03-05T12:24:16Z",
  "updated_at": "2018-06-03T06:01:45Z"
}
```

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
### 获取仓库 接口
- https://api.github.com/users/fairyly/repos?per_page=100&page=6

```
{
    "id": 81279117,
    "node_id": "MDEwOlJlcG9zaXRvcnk4MTI3OTExNw==",
    "name": "2048",
    "full_name": "fairyly/2048",
    "owner": {
      "login": "fairyly",
      "id": 17672815,
      "node_id": "MDQ6VXNlcjE3NjcyODE1",
      "avatar_url": "https://avatars1.githubusercontent.com/u/17672815?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/fairyly",
      "html_url": "https://github.com/fairyly",
      "followers_url": "https://api.github.com/users/fairyly/followers",
      "following_url": "https://api.github.com/users/fairyly/following{/other_user}",
      "gists_url": "https://api.github.com/users/fairyly/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/fairyly/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/fairyly/subscriptions",
      "organizations_url": "https://api.github.com/users/fairyly/orgs",
      "repos_url": "https://api.github.com/users/fairyly/repos",
      "events_url": "https://api.github.com/users/fairyly/events{/privacy}",
      "received_events_url": "https://api.github.com/users/fairyly/received_events",
      "type": "User",
      "site_admin": false
    },
    "private": false,
    "html_url": "https://github.com/fairyly/2048",
    "description": "A small clone of 1024 (https://play.google.com/store/apps/details?id=com.veewo.a1024)",
    "fork": true,
    "url": "https://api.github.com/repos/fairyly/2048",
    "forks_url": "https://api.github.com/repos/fairyly/2048/forks",
    "keys_url": "https://api.github.com/repos/fairyly/2048/keys{/key_id}",
    "collaborators_url": "https://api.github.com/repos/fairyly/2048/collaborators{/collaborator}",
    "teams_url": "https://api.github.com/repos/fairyly/2048/teams",
    "hooks_url": "https://api.github.com/repos/fairyly/2048/hooks",
    "issue_events_url": "https://api.github.com/repos/fairyly/2048/issues/events{/number}",
    "events_url": "https://api.github.com/repos/fairyly/2048/events",
    "assignees_url": "https://api.github.com/repos/fairyly/2048/assignees{/user}",
    "branches_url": "https://api.github.com/repos/fairyly/2048/branches{/branch}",
    "tags_url": "https://api.github.com/repos/fairyly/2048/tags",
    "blobs_url": "https://api.github.com/repos/fairyly/2048/git/blobs{/sha}",
    "git_tags_url": "https://api.github.com/repos/fairyly/2048/git/tags{/sha}",
    "git_refs_url": "https://api.github.com/repos/fairyly/2048/git/refs{/sha}",
    "trees_url": "https://api.github.com/repos/fairyly/2048/git/trees{/sha}",
    "statuses_url": "https://api.github.com/repos/fairyly/2048/statuses/{sha}",
    "languages_url": "https://api.github.com/repos/fairyly/2048/languages",
    "stargazers_url": "https://api.github.com/repos/fairyly/2048/stargazers",
    "contributors_url": "https://api.github.com/repos/fairyly/2048/contributors",
    "subscribers_url": "https://api.github.com/repos/fairyly/2048/subscribers",
    "subscription_url": "https://api.github.com/repos/fairyly/2048/subscription",
    "commits_url": "https://api.github.com/repos/fairyly/2048/commits{/sha}",
    "git_commits_url": "https://api.github.com/repos/fairyly/2048/git/commits{/sha}",
    "comments_url": "https://api.github.com/repos/fairyly/2048/comments{/number}",
    "issue_comment_url": "https://api.github.com/repos/fairyly/2048/issues/comments{/number}",
    "contents_url": "https://api.github.com/repos/fairyly/2048/contents/{+path}",
    "compare_url": "https://api.github.com/repos/fairyly/2048/compare/{base}...{head}",
    "merges_url": "https://api.github.com/repos/fairyly/2048/merges",
    "archive_url": "https://api.github.com/repos/fairyly/2048/{archive_format}{/ref}",
    "downloads_url": "https://api.github.com/repos/fairyly/2048/downloads",
    "issues_url": "https://api.github.com/repos/fairyly/2048/issues{/number}",
    "pulls_url": "https://api.github.com/repos/fairyly/2048/pulls{/number}",
    "milestones_url": "https://api.github.com/repos/fairyly/2048/milestones{/number}",
    "notifications_url": "https://api.github.com/repos/fairyly/2048/notifications{?since,all,participating}",
    "labels_url": "https://api.github.com/repos/fairyly/2048/labels{/name}",
    "releases_url": "https://api.github.com/repos/fairyly/2048/releases{/id}",
    "deployments_url": "https://api.github.com/repos/fairyly/2048/deployments",
    "created_at": "2017-02-08T02:38:16Z",
    "updated_at": "2017-02-08T02:38:19Z",
    "pushed_at": "2017-01-25T22:07:43Z",
    "git_url": "git://github.com/fairyly/2048.git",
    "ssh_url": "git@github.com:fairyly/2048.git",
    "clone_url": "https://github.com/fairyly/2048.git",
    "svn_url": "https://github.com/fairyly/2048",
    "homepage": null,
    "size": 69908,
    "stargazers_count": 0,
    "watchers_count": 0,
    "language": "CSS",
    "has_issues": false,
    "has_projects": true,
    "has_downloads": true,
    "has_wiki": true,
    "has_pages": false,
    "forks_count": 0,
    "mirror_url": null,
    "archived": false,
    "open_issues_count": 0,
    "license": {
      "key": "mit",
      "name": "MIT License",
      "spdx_id": "MIT",
      "url": "https://api.github.com/licenses/mit",
      "node_id": "MDc6TGljZW5zZTEz"
    },
    "forks": 0,
    "open_issues": 0,
    "watchers": 0,
    "default_branch": "master"
  },
```

### 获取创建组织接口
- 

## 获取 issue
- https://developer.github.com/v3/issues/

### 获取某一个仓库的 issue
- https://api.github.com/repos/fairyly/our-story/issues

### 创建一个仓库的 issue
- 



### 获取  GitHub timeline API

- https://api.github.com/users/fairyly/received_events?page=1

### 参考
- https://blog.csdn.net/qq_25537177/article/details/80561507
