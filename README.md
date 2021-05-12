# Assignment Classifier Versioning System
As you might have noticed in the screenshots a classifier can have multiple versions. The versioning system is somewhat similar to that of Git. New versions can be branched out from previous versions. An example of a versioning system of a certain classifier is shown below:

```
            * 1
            |
            * 2
           / \
        3 *   * 4
         /     \
      5 *       * 6
       / \
      /   * 7
   8 *
    / \ 10
 9 *   * -  - 
        \  \  \
         *  *  *
         11 12 13
```

Usually, a customer is not interested in all intermediate versions anymore, so it is not necessary to summarize all versions above (1-13) in a list (this is currently the case). The versioning system can be summarized in terms of the branches (versions that have no child versions yet):

```
            * 1
            |
     -  -  - -  -  -
   /  /  /     \  \  \
  *  *  *       *  *  *
  9 11 12       13 7  6

```

Also if a customer is interested in seeing the history of a specific version (and maybe revert to a previous version), it would be interesting to show the version path:

```
    1     2     4     6
    * - > * - > * - > *
```

In this assignment you will implement a class that will do the above part of the versioning system. You are free to design the exact layout of the class, but it should at least implement 3 methods:

```python
class VersioningSystem:
    
    def addVersion(self, parent):
        """
        Adds a new version to a parent version, i.e. add new version (2) to version 1.
        """
        pass

    def getBranches(self, id):
        """
        Returns a list of id's of the child versions of the branches for a given id. So for example, if id=1, this should
        return [9, 11, 12, 13, 7, 6]. The order of the returned list is not relevant in this case.
        """
        pass

    def getHistory(self, id):
        """
        Returns a list of id's that represent the history for a given id. So for example, for id=6, it should return 
        [1, 2, 4, 6]. The order of the returned list IS relevant here.
        """
        pass
```

It might be necessary to implement more methods for this class that help you to finish this assignment. Again, you are totally free to do that. A few hints to solve this assignment:

- As you probably noted, this versioning system can be represented as a network (Directed Acyclic Graph).
- It is important to keep track in you class of the parent-child relationship of th versions.
- Make sure that the versions have some sort of unique ID such that you can identify the parent and child.
- You can make sure of any library that you want to solve.
- I wrote this assignment in python, but you are free to implement the equivalent in any language you want (e.g. PHP).
- There are many ways to solve this problem, some more efficient than others. Try to make sure that you have the right solution first. Efficiency is less important.

You can text/email/call me for questions.

Good luck! 