This class stores the user data. Storing the user id in the ‘id’ variable and ‘websites’ variable stores the websites of the user in instance of our entity class as key-value Pairs, Keys being the Company name and value being the instance of the Class Website storing the website info.
Functions:
    • addWebsite() : adds the given website object in our ‘websites entity’ with company name being the id and the given object website as the value .
    • DeleteWebsite (): Deletes the website (VALUE) associated with given company name( KEY)
    • getWebsite () : Returns the website associated with the given company name
    • selectwebsite() : Selects the website associated with the given Company name by setting the selectedData variable of ‘websites’(ENTITY class object) to the website object
    • getSelectedWebsite() : Returns the selected Website obejct.
