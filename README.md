## CouncilWise integration
Customers that use councilwise integration were previously able to add a parameter their Pozi URL ?propnum=1234. We have removed the ability to pass parameters that way and this has broken the council wise integration.

In council wise the admin would create a link-in URL to Pozi and pass the property number value from the property screen. In Pozi a link-in that we would expect the user to use would look like this https://sitename.pozi.com/#/map[enterprise]/search[assessmentnumber,{data-id}]. However CouncilWise throws an error when that URL is included.

## What does this redirect page do?
Because the Pozi URL wont load in the Council Wise UI. We have had to create a redirect page that contains all the parameters needed to build the Pozi map URL.

The redirect page simply creates the URL and loads it for the user.

The redirect page is accessible at: [https:](https://andrew-chartis.github.io/councilwise-redirect/?) 
The redirect page takes the following parameters:
* config: Values are "legacy" or "sitemanager". Usage - config=legacy
* site: The name of your pozi site. Usage - site=demo
* map (required for config=sitemanager): The name of the map you want to load. Usage - map=enterprise
* search: The name of the search you want to link-in to. Usage - search=searchname
* id: This is the councilwise parameter and must be of value {data-id}

So a formatted URL in councilwise would look like this:
Site Manager site
https://andrew-chartis.github.io/councilwise-redirect/?config=sitemanager&site=sitename&map=enterprise&search=assessmentnumber&id={data-id}

Legacy Site
https://andrew-chartis.github.io/councilwise-redirect/?config=legacy&site=sitename&search=propertynumber&id={data-id}
