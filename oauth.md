From [Oauth 2.0 Primer](https://www.youtube.com/watch?v=996OiexHze0)

3 actors
  -Resource Owner : the end user
  -Client         : The application
  -Authorization Owner: The party that stores and controls access to the resource being sought by the client

Flow
![Oauth 2.0 Basic Flow](images/Outh2_0.png)

- Request access from Resource Owner for resource (//grant access to google contact list)
- On approval client sends a request to authorization server w scope as the resource in question
- Resource owner logs into authorization app and asked to provide ```consent``` client request for the resource
- On confirmation authorization server ```grant```s the auth code to the client
- The client uses the auth code in addition to the secret key access the resource

Open ID Connect - Adds authentication standard to Oauth2.0
![OpenID Connect](images/OpenIDConnect.png)
