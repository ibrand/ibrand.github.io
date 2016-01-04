---
title:  "Interview Utility Belt"
description: The three tricks I use at tech interviews
## date: 2016-01-04
---

I recently did a handful of tech interviews. As I went along I picked up a few tricks from failures and successes that I reused at other interviews.

I will walk through each of them in order of importance/how useful I actually found them to be:

## Maps
Maps were helpful in almost every problem I encountered while interviewing. This was particularly true for optimizing an answer and could usually bring it to an O(n) runtime.

You can often cache results in a map for expensive computations and then access those results later with an O(1) look up time. While caching can give a fast look up time, it is detrimental if you're trying to optimize for space. Interviewers do ask about space efficiency once in a while and it is good to be aware that a map is spatially inefficient.

One thing I would often mention in my interviews is that it would be a great thing to have a map if we were planning on reusing the function many times. It doesn't matter if you build up a large map once (which can take a lot of time) if you're planning on using the function that searches the map a lot of times.

## Sorting the input
A good place for me to start thinking about problems related to strings and arrays was to think about how I might solve the problem if the input was sorted.

Sorted input is often a lot easier to problem solve with and yields faster solutions. Sorting input will put your solution at at least an O(n log n) runtime because sorting algorithms themselves take that much time, but that's not such a bad starting point.

## Garbage Input
If you're not using a piece of an array or string anymore you can overwrite it!

There might be problems that come up where you're required to move characters or elements around in arrays and strings. In order to be the most time and space efficient you want to aim for O(n) runtime and do the operation in-place. If you know that you wont need the items at the beginning of the array/string anymore you can just write over them in-place. Thinking about overwriting waste can be a helpful tool when thinking through a problem.

## Conclusion
All of these tools served to shift my mindset when interviewing and gave me different modes of approaching a problem. Often, an answer would not come immediately so it was helpful to think about different ways of framing the problem in hopes that reshuffling the input will yield an "aha!" moment.

I figured these things out through my own trial and error while working through interview problems both on [leetcode](https://leetcode.com/) and in real interviews. It was helpful for me to note which tactics seemed useful and generalizable at the end of each problem to strengthen myself for the next one.

