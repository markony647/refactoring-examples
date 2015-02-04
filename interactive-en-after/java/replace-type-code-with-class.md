Let's look at <i>Replace Type Code With Class</i>, using the example of a person class that contains blood type fields.

Blood types are coded as four constants of this class.

We start refactoring by creating a new <code>BloodGroup</code> class, which will be responsible for blood types.

We place the blood type field from the <code>Person</code> class, its getter and the constructor, which initialize the field value.

Now let's create static methods for each of the type code values from the original class. These methods should return instances of the <code>BloodGroup</code> class.

Let's compile and test our code.

In the original class, change the type of the coded field to <code>BloodGroup</code>.

Change the code of the constructor and setter accordingly.

Then change the field getter so that it calls the getter of the <code>BloodGroup</code> class.

It is now time to replace all type code values with calls to the corresponding static methods of the <i>type class</i>.

First replace the values of all constants with calls to the corresponding methods of the <code>BloodGroup</code> class.

In effect, all uses of constants are now delegated to the methods of <code>BloodGroup</code>.

We will go one step further and get rid of direct references to constants of the <code>Person</code> class in the remaining code. We can use calls to the methods of the <code>BloodGroup</code> class instead.

After all the changes, test everything carefully.

In the end, it is better to avoid using any numeric codes for <code>BloodGroup</code> and use objects instead. Let's try to do so in the <code>Person</code> class.

These changes will probably cause the client code to break, but this can be fixed by simply getting rid of the codes there as well.

And finally, remove the constants from the <code>Person</code> class.

Let's perform the final compilation and testing.

The refactoring is complete! You can compare the old and new code if you like.