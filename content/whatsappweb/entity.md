+++
title = "Entity"
description = ""
weight = 1
+++

This class uses `Map` to store data in key-value pairs. It keeps track of the number of data and selected data.

{{< panel title="Properties" style="primary" >}}

    {{< listItems data selectedData count >}}

{{< /panel >}}

{{< panel title="Methods" style="primary" >}}

    {{< listItems "addData(key, value)" "isData(key)" "deleteData(key)" "clearData()" "selectData(key)" "getData(key)" "getAllData()"  >}}

{{< /panel >}}

### Properties
<hr>

{{< prop title="data" type="Map" >}}

A Map() object that stores the data.

{{< prop title="selectedData" type="string" >}}

The selected data is actually the key of the data selected.

{{< prop title="count" type="string" >}}

Keeps track of the number of key-value pairs.

### Methods
<hr>

{{< prop title="addData(key, value)" type="boolean" >}}

Add the given key-value pair into the `data` variable and `selectedData` is assign to the newly created key. 

{{< prop title="isData(key)" type="boolean" >}}

Check if a value is mapped to a given key in the `data`

{{< prop title="deleteData(key)" type="boolean" >}}

Deletes the key-value pair from the `data` of the given key

{{< prop title="clearData(key)" type="void" >}}

Deletes all the key-value pairs in the `data`.

{{< prop title="selectData(key)" type="boolean" >}}

Assigns the `selectedData` to the given key

{{< prop title="getData(key)" type="object" >}}

Returns the value for the given key. Returns null if a value does not exist for the given key.

{{< prop title="getAllData(key)" type="object" >}}

Returns the `data`.