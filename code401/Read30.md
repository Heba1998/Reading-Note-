# Hashtables

![](https://i.imgur.com/bEIWPaQ.png)

## What is a Hashtable?

*technique that is used to uniquely identify a specific object from a group of similar objects.*

*Hashtables are a data structure that utilize key value pairs. This means every `Node` or `Bucket` has both a key, and a value*

* **Terminology:**

    * **Hash** - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
    * **Buckets** - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
    * **Collisions** - A collision is what happens when more than one key gets hashed to the same location of the hashtable.


![](https://i.imgur.com/2ON8Kt5.jpeg)

* **complexity**

*Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.*

*Arrays actually have fast access. If we know the index of the information we want we can access that information in O(1) time. The reason why searching for a piece of data in a collection is O(N) isn’t because the array is slow, it’s just that we have to look through all N things in the collection.*



* **What is the benifits of Hash ,Buckets,Collisions**
    * Hold unique values
    * Dictionary
    * Library

* **Internal Methods :**
    * Add()
    *  Find()
    * Contains()
    * GetHash()