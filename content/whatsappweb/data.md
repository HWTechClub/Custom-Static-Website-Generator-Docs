+++
title = "StructuredData"
description = ""
weight = 2
+++

This class stores all the user data. It uses an instance of `Entity` class to store the `User` instances. Currently, the app uses only one instance of this class as a global class named `data`.

{{< panel title="Properties" style="primary" >}}

    {{< listItems entity >}}

{{< /panel >}}

{{< panel title="Methods" style="primary" >}}

    {{< listItems "addUser(user)" "getUser(id)" "deleteUser(id)" " isUser(id)" "clearData()" >}}

{{< /panel >}}

### Properties
<hr>
{{< prop title="entity" type="Entity" >}}

Entity stores data using `Map` with some extra functionality.


### Methods
<hr>

{{< prop title="addUser(user)" type="boolean" >}}

Adds the user to the dataset.
Returns `true` if a the user is succefully added. 
Returns `false` if the user is not added.

{{< prop title="getUser(id)" type="User" >}}

Gets the user from the dataset using its id.

{{< prop title="deleteUser(id)" type="boolean" >}}

Deletes the user from the dataset with the user id.
Returns `true` if a the user is succefully deleted. 
Returns `false` if the user is not deleted.

{{< prop title="isUser(id)" type="boolean" >}}

Check if a user with the given id exists

{{< prop title="clearData()" type="void" >}}

Clears all the data stored