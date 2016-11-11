# OAuth 2.0 

In SharePoint online, Office 365 and Azure AD, the OAuth 2.0 protocol is used for Authentication,      there are various ways you can implement it for different situations but it all usually comes down to the fact you are getting an access token.
If you come to me, Office 365, with a token that says you are authenticated, if that token was obtained from Azure AD, then I will trust what it says about you

# What data access token contain.
Aside from some metadata in the token such as the type of token (typ=JTW) and how it was digitally signed (alg=RSA256), you’ll find information about this like who the issuer is (is), the id of the Azure AD tenant that was responsible for the authentication of the user (tid=[guid]) and the ID of the application in Azure AD (appid=[guid]).
The token will also tell you when it is valid, such as what time it was issued (iat=[seconds since Nov, 2016 UTC]), when the token starts being valid (nbf=[seconds since Nov 1, 2016 UTC]) and when it is valid until (exp=[seconds since  Nov 1, 2016 UTC].
There is also a little information about the user who did the authentication in the family name, given name, unique name= & upn = [email login]
