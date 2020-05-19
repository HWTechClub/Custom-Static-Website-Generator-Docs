+++
title = "Create website"
description = ""
weight = 2
+++

## Single template
At the current moment we only have one template which is a e-commerce template.

### 1. POST: /generate
Body:
{{< code lang="js" >}}
{
  firstName: "",
  lastName: "",
  companyName: "",
  logoUrl: "",
  bannerUrl: "",
  email: "",
  description: "",
  template: "Colo_Shop",
  csv: ""
};

//Ex : csv columns: "product id,product name,description,cost,product image url \n 1, test,test desc,120,https://test/test.png


{{< /code >}}

Response:
{{< code lang="js" >}}
{
    'directory': result
}

{{< /code >}}


Append result to :
{{< code lang="js" >}}
<ip address:port no>/pages/<result>
{{< /code >}}

### 2. GET: /ipfsdeploy
Parameter :
{{< code lang="js" >}}
id = <result>

//ex : <ip address:port no>/ipfsdeploy?id=<result>
{{< /code >}}

Response:

{{< code lang="js" >}}
{
    'data': hash <id>
}

//Ex : ipfs.io/ipfs/<hash>

{{< /code >}}
