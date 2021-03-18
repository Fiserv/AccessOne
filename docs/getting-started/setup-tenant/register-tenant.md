# Register the tenant

Now that the tenant is configured and deployed we now need to register the URL with the `Fiserv Developer Portal.`

Head to [Tenant Registration](https://developer.fiserv.com/tenant)

After you fill in the requested information your tenant will now show in the `Fiserv Developer Portal`.

Head to [Fiserv Developer Portal](https://developer.fiserv.com)

You will find your tenant under the `Solution` area you designated in the `tenant.json` configuration file.

Congratulations, you've got a working tenant in the `staging` system.

To have your tenant show up in the `production` system finish editing your content and simply `publish` it to the `main` branch in your repositry.  More on that can be found in the [Preview vs Publish](../preview-and-publish-tenant.md)