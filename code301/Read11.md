#  Authentication


## What is OAuth:


![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTe8nKTBjYHMyf8wmK-AEGIFfxQA3IGDZhE6Q&usqp=CAU)



* *What is OAuth?*

`OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial`

* *Give an example of what using OAuth would look like.*

`The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon.`


* *How does OAuth work? What are the steps that it takes to authenticate the user?*

![img](https://a.slack-edge.com/fbd3c/img/api/articles/oauth_scopes_tutorial/slack_oauth_flow_diagram.png)

```
Let’s assume a user has already signed into one website or service (OAuth only works using HTTPS). The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens (greatly simplified):

1- The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.

2- The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.

3- The first site gives this token and secret to the initiating user’s client software.

4- The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).

5- If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.

6- The user approves (or their software silently approves) a particular transaction type at the first website.

7- The user is given an approved access token (notice it’s no longer a request token).

8- The user gives the approved access token to the first website.

9- The first website gives the access token to the second website as proof of authentication on behalf of the user.

10- The second website lets the first website access their site on behalf of the user.

11- The user sees a successfully completed transaction occurring.

12- OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
```

* *What is OpenID?*

`ID avalible and can be freally used`



## Authorization and Authentication flows: 


![img](https://1tskcg39n5iu1jl9xp2ze2ma-wpengine.netdna-ssl.com/wp-content/uploads/2020/02/oauth-2-flow-diagram.png)



* *What is the difference between authorization and authentication?*


`Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.`


* *What is Authorization Code Flow?*

`exchanges an Authorization Code for a token.`

* *What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?*

`exchanges an Authorization Code for a token.`


* *What is Implicit Flow with Form Post?*

`is intended for Public Clients, or applications which are unable to securely store Client Secrets.`

* *What is Client Credentials Flow?*

`With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user. For this scenario, typical authentication schemes like username + password or social logins don’t make sense. Instead, M2M apps use the Client Credentials Flow`

* *What is Device Authorization Flow?*

`With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. This avoids a poor user experience for devices that do not have an easy way to enter text. To do this, device apps use the Device Authorization Flow , in which they pass along their Client ID to initiate the authorization process and get a token.`

* *What is Resource Owner Password Flow?*

`it's request that users provide credentials (username and password), typically using an interactive form. The Resource Owner Password Flow should only be used when redirect-based flows (like the Authorization Code Flow) cannot be used.`