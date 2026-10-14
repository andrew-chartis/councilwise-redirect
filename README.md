## CouncilWise integration
Customers that use councilwise integration were previously able to add a parameter their Pozi URL ?propnum=1234. We have removed the ability to pass parameters that way and this has broken the council wise integration.

In council wise the admin would create a link-in URL to Pozi and pass the property number value from the property screen. In Pozi a link-in that we would expect the user to use would look like this https://sitename.pozi.com/#/map[enterprise]/search[assessmentnumber,{data-id}]. However CouncilWise throws an error when that URL is included.
