Download Link: https://assignmentchef.com/product/solved-cmsc204-project-5-classes-required-to-create-a-morse-code-converter-utility
<br>



Project 5

Write the classes required to create a Morse Code Converter Utility. Your Morse Code Converter Utility will be using a generic linked binary tree with generic TreeNodes to convert Morse Code into English. There is no GUI requirement for this assignment. You are supplied a GUI for testing purposes.

<strong>Academic Honesty Policy Reminder</strong> | <strong>Do your own work</strong> – each submitted project will be compared against other submissions from current and previous semesters.

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Concepts tested by this assignment</strong></td>

  </tr>

 </tbody>

</table>




Generic Classes

Utility Class (all static methods)

Linked Trees

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Classes</strong></td>

  </tr>

 </tbody>

</table>

Building a Tree for conversion purposes

<strong>Data Element – </strong><strong>TreeNode class</strong>

This generic class is used in the MorseCodeTree classes.  The class consists of a reference to the data and a reference to the left and right child.  Follow the Javadoc that is provided.  The Javadoc only lists those public methods that are required to pass the Junit tests.  You may add any private methods you need for your design.

<strong>Data Structure – MorseCodeTree class</strong>

A generic linked binary tree which inherits from the LinkedConverterTreeInterface.  The class uses an external generic TreeNode class parameterized as a String: TreeNode&lt;String&gt;.  This class uses the private member of root.  Nodes are added based on their morse code value.  A ‘.’ (dot) means to traverse left and a ‘-‘ (dash) means to traverse right. The constructor will call the method to “build the tree”.  Follow the Javadoc that is provided. The Javadoc only lists those public methods that are required to pass the Junit tests.  You may add any private methods you need for your design.

<strong>Utility class – MorseCodeConverter</strong>

The MorseCodeConverter contains a static MorseCodeTree object and constructs (calls the constructor for) the MorseCodeTree.

This class has two static methods <em>convertToEnglish</em> to convert from morse code to English. One method is passed a string object (“.-.. — …- . / .-.. — — -.- …”).  The other method is passed a file to be converted.  These static methods use the MorseCodeTree to convert from morse code to English characters.  Each method returns a string object of English characters.

There is also a static printTree method that is used for testing purposes – to make sure the tree for MorseCodeTree was built properly.

Use the Javadoc provided to make sure that your MorseCodeConverter class follows the method headers so that the MorseCodeConverterTest will run correctly.

<strong>Testing – </strong><strong>JUnit Test Classes</strong>

You must add at least 1 test for MorseCodeConverter.convertToEnglish(String) and at least 1 test for MorseCodeConverter.convertToEnglish(File) to the MorseCodeConverterTest class.  You must create a JUnit test for your MorseCodeTree class. Include your test files with your code files.

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Assignment Details</strong></td>

  </tr>

 </tbody>

</table>




This is a table for the conversion from Morse Code to alpha letters.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/674.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/674.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<strong>Building the MorseCodeTree (method buildTree)</strong>

Your MorseCodeTree is a 4 levels tree.  Insert a mapping for every letter of the alphabet into the tree map.  The root is a TreeNode with an empty string.  The left node at level 1 stores letter ‘e’ (code ‘.’) and the right node stores letter ‘t’ (code ‘-‘).  The 4 nodes at level 2 are ‘i’, ‘a’, ‘n’, ‘m’ (code ‘..’, ‘.-‘, ‘-.’, ‘—‘).  <strong>Insert</strong> into the tree by tree level from left to right.  A ‘.’ will take the branch to the left and a ‘-‘ will take the branch to the right.  This is the structure of the tree.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/443.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/05/443.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<strong>Using the MorseCodeTree</strong>

Use the MorseCodeTree to convert Morse Code to English by taking the code and finding it’s corresponding English letter by traversing the MorseCodeTree, ‘.’ branches to the left and ‘-‘ branches to the right.  The code ‘.–.’ would branch to the left, then to the right, then to the right, then to the left to <strong>Fetch</strong> the letter ‘p’.  Each letter is delimited by a space (‘ ‘).  Each word is delimited by a ‘/’.