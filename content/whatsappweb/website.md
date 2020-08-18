+++
title = "Website"
description = ""
weight = 5
+++

It stores all the data of a user's website and its products. 
{{< panel title="Properties" style="primary" >}}

    {{< listItems firstName lastName companyName logo banner logoUrl bannerUrl desc email products >}}

{{< /panel >}}

{{< panel title="Methods" style="primary" >}}

    {{< listItems "addProduct(product)" "getProduct(productId)" "getAllProduct()" "deleteProduct(productId)" "selectProduct(productId)" "getSelectedProduct()" "toJson()" >}}

{{< /panel >}}

### Properties 
<hr>

{{< prop title="products" type="Entity" >}}

Stores the products of the website.

### Methods 
<hr>

{{< prop title="addProduct(product)" type="boolean" >}}

Add the given product to the `products`

{{< prop title="getProduct(productId)" type="Product" >}}

Returns the product with the given id.

{{< prop title="getAllProduct()" type="Iterable<Product>" >}}

Returns all the product

{{< prop title="deleteProduct(productId)" type="boolean" >}}

Deletes a product with the `productId`

{{< prop title="selectProduct(productId)" type="Product" >}}

Selects a product with the given id

{{< prop title="getSelectedProduct(productId)" type="Product" >}}

Returns the selected product

{{< prop title="toJson(productId)" type="string" >}}

Converts the instance of the `Website` class into a JSON string. The products are stored in the JSON in the CSV format. Returns the JSON string at the end of the function.

