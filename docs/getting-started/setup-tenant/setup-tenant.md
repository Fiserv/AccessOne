# Setup a tenant

Products within the Fiserv portfolio that are showcase through the portal are known as `tenants`.  Tenants standup a `tenant server` that will serve all the content through the portal to developers visiting the Fiserv Developer Portal.

## Cloning the Github tenant repoistory

An example Github repository has already been prepared for you to clone.

Head to [Sample tenant repo](github.com/fiserv/sample-tenant) and create a new repoisotry based on this by using the 'New' button.

Your repo name should match your product name.

You've not got a tenant repoistory.

## Configure your tenant

Now that you've got your repoistory we need edit the configuration files.

Two main files will need to be edited for the Fiserv Developer Portal to load the tenant data properly.

Your edits will be made in the `develop` branch.

### Edit the tenant.json

The `tenant.json` contains metadata information about your product.

The file is located, from the repoistiory root, `/config/tenant.json`.

.....

### Edit the layout.yaml

The `layout.yaml` determines what you want to display on your `product overview page`.

The file has several sections for each card that shows on the product overview page.

.....

## Connect Stoplight

To make creating or editing your content easier we're going to connet your Github repoistory to Stoplight.io.

Head to the [Fiserv Stoplight](fiserv-portal.stoplight.io) and signup.

Once you're there create a project with the same name as your product.

Then head into the settings to connect your github.

## Create your content

You can go into `Stoplight Studio` to create your API specification or markdown files.

### API Specification

Your API specification will need to be stored in the `/reference` folder.

The file name should follow your API version, i.e. `api-1.0.3.yaml`

This folder should hold multiple API version files.

### Markdown documentation

All the documentation files follow the Markdown guides, which you can find here [Markdown Support](../../resources/markdown-support.md)

Details on the folder structure are [here](../../resources/folder-structure.md)

For now you can edit the existing sample `getting-started.md` file.

## Recap

You've now got
* Your Github repoistory cloned
* Your tenant config files have been edited
* Stoplight is connected to the repoistory
* You have an API specification file and markdown files edited

## Next steps

[Deploy tenant](./deploy-tenant.md)