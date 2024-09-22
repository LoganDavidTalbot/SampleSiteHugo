# SampleSiteHugo


## Links

- [Hugo](https://gohugo.io/)
- [Hextra](https://imfing.github.io/hextra/docs/guide/deploy-site/)
- [Static Web App Authentication](https://learn.microsoft.com/en-us/azure/static-web-apps/authentication-authorization#block-an-authentication-provider)
- [Static Web App Auth Entra Id](https://learn.microsoft.com/en-us/azure/static-web-apps/authentication-custom?tabs=aad%2Cinvitations)


```
{
  "routes": [
    {
      "route": "/test",
      "allowedRoles": ["authenticated"]
    }
  ],
  "responseOverrides": {
    "401": {
      "statusCode": 302,
      "redirect": "/.auth/login/aad"
    }
  },
  "auth": {
    "identityProviders": {
      "azureActiveDirectory": {
        "registration": {
          "openIdIssuer": "https://login.microsoftonline.com/<TENANT_ID>/v2.0",
          "clientIdSettingName": "AZURE_CLIENT_ID",
          "clientSecretSettingName": "AZURE_CLIENT_SECRET_APP_SETTING_NAME"
        }
      }
    }
  }
}

```