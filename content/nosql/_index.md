---
draft: false
title: "Creating a NoSQL database on Azure"
---

# 0. Introduction

In this tutorial we will set up a database and fill it with records containing information about the periodic table of elements. In a subsequent tutorial, we'll build an API for the public to access this database (without needing to log in to your Azure account 😉).

Specifically, we'll be using a NoSQL database (pronounced "no-seek-well") using Azure's "CosmosDB" service. NoSQL databases are great ways to store 

This guide assumes that you've completed the [VM Workstation tutorial](../workstation). If you haven't, go back and skim through it now. Using a remote VM is not required to do any of the things outlined in this tutorial, but it _will_ make it easier for course staff to help you debug things.

# 1. Open the Azure portal

TODO description

{{% aside %}}
🔗 [https://portal.azure.com](https://portal.azure.com)
{{% /aside %}}


# 2. Create an empty database

TODO

![](./img/az-search-cosmos.png)

![](./img/az-cosmos-dash.png)

![](./img/az-create-nosql.png)


TODO
- sub: TODO
- rg: TODO
- name: `______-periodic-db` w uwnetid
- location: West US 3 (same as workstation vm, generally a good idea)
- Apply Free Tier Discount: Do **Not** Apply

![](./img/az-create-db-general.png)


`Next: Global Distribution >`

- Geo-Redundancy: Disable 
- Multi-region Writes: Disable

`Next: Networking >`

word about security

`Review + Create`

Click blue create button.

Wait a bit and click `Go to resource`:

![](./img/az-cosmos-created.png)


automatically goes to quickstart, boo. go to data explorer instead:

![](./img/az-cosmos-quickstart.png)


![](./img/az-new-container.png)

Choose --
  - Create new database, id `periodic-db`
  - Container id `elements`
  - Partition key `/Period`. Talk about even scaling
  - Max RU/s: 1000. Talk about RU estimation (read ~ 1 RU, write ~5 RUs)
  
![](./img/az-cosmos-container-options.png)

Click OK at bottom

If all good:
![](./img/az-cosmos-empty-container.png)

Let's put some stuff in it!

# 3. Populate the database

TODO

Name folder `db-populate`:

![](./img/vm-new-folder.png)

Name file `requirements.txt`:
![](./img/vm-new-file.png)


![]()
![]()

# 4. Querying the database

TODO

