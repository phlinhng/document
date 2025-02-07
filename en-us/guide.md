# User Guide

Please read and accept our Term of Service then go to the next step. Once you done so, it means that you agree with our Term of Service.

The usage of FastGit is basically relate on `git` . For common GitHub operations, you can use the command `clone` like:

```bash
git clone https://github.com/author/repo
```

To use FastGit, you change it into:

```bash
git clone https://hub.fastgit.org/author/repo
```

Just like what you see, FastGit is physically a proxy of GitHub, and what you need to do is just replacing the URL.

You can also edit `git` configurations to take an easier way to use our service.

> **Note**  
> You will fail to push or to do other operations which need your authorization after you turn FA2 on. (Whatever you use access token as your password) This is caused by the standardization of GitHub.

With the growth of FastGit, we will deploy more resources to support our speed-up service. You can find the list of our nodes in the chapter [Nodes](../en-us/node.html).

## The Usage of Web

FastGit also supplies basic supports for the common GitHub Web operations. You can directly access nodes with Web supports.

Due to the safety concerns, we banned things which are sensitive, like `Cookie` and `Session` . That means you are not able to do sensitive operations such as signing in GitHub via FastGit.

## Download Releases or Source Code Archive

For common `clone` and `push` operations, FastGit already have provided perfect support. We can use the command below to download releases & source code archive.

```bash
# Release
# If your downalod link is: https://github.com/A/A/releases/download/1.0/1.0.tar.gz , then you use:
wget https://download.fastgit.org/A/A/releases/download/1.0/1.0.tar.gz

# Codeload
# If your download link is: https://hub.fastgit.org/A/A/archive/master.zip
# or https://codeload.github.com/A/A/zip/master
wget https://download.fastgit.org/A/A/archive/master.zip
```

## SSH Clone

~~We also support SSH clone. Just replace github.com to fastgit.org to enjoy.~~

Due to some unresistible factors, we don't provide SSH clone service.

### FAQ

**Q:** Why can't I download files directly from `hub.fastgit.org`?

**A:** Because there are not having a method to solve the special situations such as HTTP 301 returns during caching releases with only NGINX configurations yet. (PS: If you have an idea, please tell us via `issue` ) Also, we didn't enable cache for `hub.github.com` . If you need to download a release, just use `download.fastgit.org` .

**Q:** Why can't I clone using `download.fastgit.org` ?

**A:** Because we enable cache of `download.github.org` , and there would be a difference between the copy you get from FastGit comparing to the original repo. Anyway, we wouldn't stop you from doing that way. You should notice that we've added `keep-alive` for `hub.github.org` and you can clone over there with usually a faster speed than the release one.

## For the Raw Proxy

We also have proxy for <https://raw.githubusercontent.com/> .  
The URL is: <https://raw.fastgit.org/> .
