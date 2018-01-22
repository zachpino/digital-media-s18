###Week 1: Assign and Address with AWS

-----

The [server is now running](server.md), but we can neither access its files nor find it on the internet. In order to find the machine on the internet, we need to give it an address.

Inside of the EC2 Dashboard, which is accessible within the AWS `Services` menu under `Compute`, select `Elastic IPs` in the `Network & Security` menu group. Initially the screen will be empty.

- Click `Allocate New Address` 
- On the strange interstitial screen with no options, click `Allocate`

A new [IP address](https://en.wikipedia.org/wiki/IP_address), in the form ###.###.###.### will be created for you. IP addresses allow entitites on the internet to find one another, and this set of numbers will be the location of your class website. Copy the address you created to a safe place.

- Select the `Actions` button and `Associate Address`
- Under `Instance` select the long alphanumeric string that represents your EC2 virtual server.
- Click `Associate`

Now that our server is reachable at that IP address, we can [prepare an identity file](identityfile.md) for connecting our server. Make a record of your IP for future use.
