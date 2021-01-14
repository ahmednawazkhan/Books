## Chapter 19: Policy and Level

Policies that change for the same reasons, and at the same times, are at the same level and belong together in the same component. Policies that change for different reasons, or
at different times, are at different levels and should be separated into different components

The art of architecture often involves forming the regrouped components into a directed acyclic graph

A strict definition of “level” is “the distance from the inputs and outputs.” The farther a policy is from both the inputs and the outputs of the system, the higher its level. The policies that manage input and output are the lowest-level policies in the system

* Example of Encryption

```c++
function encrypt() {
    while(true)
    writeChar(translate(readChar()));
}
```
This is incorrect architecture because the high-level `encrypt` function depends on the
lower-level `readChar` and `writeChar` functions

Recall that policies are grouped into components based on the way that they change. Policies that change for the same reasons and at the same times are grouped together by the SRP and CCP. Higher-level policies—those that are farthest from the inputs and outputs—tend to change less frequently, and for more important reasons, than lower-level policies. Lower-level policies—those that are closest to the inputs and outputs—tend to change frequently, and with more urgency, but for less important reasons
