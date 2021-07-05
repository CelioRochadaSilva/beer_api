<h2>#1</h2>

Your processor is: jdk.proxy2.$Proxy27



In my case, I had a dependency module running in the project that used another version of lombok. Another spring-boot version to be more precise. With it's BOM comes another lombok version.

[![version warning](https://i.stack.imgur.com/CFOfl.png)](https://i.stack.imgur.com/CFOfl.png)



<h2>#2</h2>

$ git push -u origin master
remote: Password authentication is temporarily disabled as part of a brownout. Please use a personal access token instead.
remote: Please see https://github.blog/2020-07-30-token-authentication-requirements-for-api-and-git-operations/ for more information.
fatal: unable to access 'https://github.com/sabrinagobel/beer_api.git/': The requested URL returned error: 403

Solution:

1. Generate a new token from git [dev settings](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)
2. Remove and re-add origin locally `git remote remove origin`
3. `git remote add origin https://<token>@<git_url>.git`

