---
title: Frequently Asked Questions
category: help
order: 1
---

1. [What should I fill in for Auth username and Auth password?](#what-should-i-fill-in-for-auth-username-and-auth-password)
2. [How to enable Basic Authentication](#how-to-enable-basic-authentication)
3. [I'm getting error that says "Unable to establish connection with ZooKeeper."](#im-getting-error-that-says-unable-to-establish-connection-with-zookeeper)

---

##### What should I fill in for Auth username and Auth password?

Auth username and password are optional, so feel free to leave those empty. Every username & password pair entered (you can enter many) serves as an extra ACL identity, so ZNodes can be given some permissions only for users logged in with certain credentials.

---

##### How to enable Basic Authentication?

At the moment there is no configuration option to enable Basic Auth out-of-the-box. 

I suggest placing a proxy which supports Basic Auth in front of ZooNavigator. For example [Traefik](https://docs.traefik.io).

---

##### I'm getting error that says "Unable to establish connection with ZooKeeper."

ZooNavigator cannot find ZooKeeper host(s) using the connection string you entered in the connect form. 

**Windows and Mac users:**  
If you're trying to access ZooKeeper running locally on host machine (not in Docker container), [follow this advice](https://github.com/elkozmon/zoonavigator/issues/40#issue-495910852).