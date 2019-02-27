# spring-boot-security-oauth2-resource-server

This is a simple Resource Server which work independent of any Authentication Server.
You can integrate with any Authentication Server.

## NOTE:
1. You first have to get valid TOKEN from your AS.
2. That AS you use must have a call which will return principal. That call has to be specified in **_userInfoUri_** property in **application.yml**
3. In my case my authetication server returns java.security.Principal object via this Get call https://apis.innowi.com:81/v1/demo/merchant/verify_token, you have to replace with yours.
4. sample Principal response from AS is like:
```
{
    "password": null,
    "username": "some.username@email.com",
    "authorities": [
        {
            "authority": "ROLE_USER"
        }
    ],
    "accountNonExpired": true,
    "accountNonLocked": true,
    "credentialsNonExpired": true,
    "enabled": true
}
```
