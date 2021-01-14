### Chapter 23: Presenters and Humble Objects

#### The Humble Object Pattern

Split the behaviors into two modules or classes. One of those modules is humble; it contains all the hard-to-test behaviors stripped down to their barest essence. The other module contains all the testable behaviors that were stripped out of the humble object


Using this pattern we can split UI into PRESENTERS 
(The Presenter is the testable object. Its job is to accept data from the application and format it for presentation so that the View can simply move it to the screen)
and VIEW (humble object that is hard to test)

<ins>
At each architectural boundary, we are likely to find the Humble Object pattern lurking somewhere nearby. The communication across that boundary will almost always involve some kind of simple data structure, and the boundary will frequently divide something that is hard to test from something that is easy to test. The use of this pattern at architectural boundaries vastly increases the testability of the entire system
</ins>