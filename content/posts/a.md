---
title: "Foreign Language Learning Applied To Programming"
date: 2019-02-05T21:03:12-08:00
draft: false
---


Studying and using foreign languages for most of my career may have skewed the lense I look at learning anything through, but I can't help but feel that programmers, who frequently find themselves having to learn new language and concepts could benefit from many techniques and methods developed for second language acquisition. I plan to explore tools and ideas for making learning programming easier in this series of posts.

One objection that I imagine many programmers might have to the suggestion learning programming should be anything like learning a second language is that learning programming is primarily about understanding the concepts whereas language learning is more about rote memorization of vocabulary items. I understand this objection since programming at its best to me often feels like constructing simple machines based on logical first principles, not regurgitating memorized information. I suspect though that as programmers we are only free to feel that sense of operating on pure logic precisely because our brains are doing some work behind the scenes to allow us to compose memorized chunks of syntax and technique into larger pieces.

When working to solve a basic algorithm challenge like “find all duplicate entries in an array of numbers”, my first thought is NOT “an array is a series of equally sized values laid out contiguously in memory that we can iterate through by memory addresses at integer multiples of the size of one element….” That is probably too low on the abstraction level and could potentially turn a 5 minute problem into a 30 minute problem. Hopefully the first thought that occurs to me is “ok we will use some kind of hash table like structure to keep a count of seen items”. My preferred code for doing that is something like:
<pre><code>
let map = {}
for(let i = 0; i < nums.length; i++){
	map[nums[i]] = (map[nums[i]] || 0 ) + 1;
}
</code></pre>

But I have used this code so many times that I don’t really have to think about it. As competitive programmers say the algorithms should be almost in your fingers. So I am able to think at the level of abstraction of “while counting the entries in the array as soon as we see a duplicate add it to some structure like a list or array” and the problem is most of the way to being solved.

Given the way of thinking of programs as small abstract chunks, to what extend would we as programmers benefit from practicing these small abstract chunks? Sonewhere between “not at all” and that we should study them exclusively is probably the answer. It probably is true that that harder part of learning programming will always be the conceptual part and that seems to be most effectively instilled by needing to use the concept to solve a real world problem rather than learning it in a artificial drill environment.

The often heard advice that goes something like “learn the basic syntax and go build something” clearly works and is not bad advice as thats how many people seem to have learned to program. But having learned foreign languages systematically using vocabulary drills, mnemonics, and spaced repetition to learn vocabulary at a rate of 100s of words per week I wonder if we are leaving potential efficiency gains on the table not only in learning new languages but also in switching back to languages we may have become rusty in.

I have been thinking of compiling something like “most commonly used 1 to 3 line code snippets of Python” because Python in particular I use just enough that I never can remember the syntax quirks and method names. I have no idea what percent of Python one needs to know to be effective that this would cover but my guess is that programming languages are actually much more repetitive and susceptible to this kind of drilling/practice than natural languages if you are not bogged down by learning new concepts.

To test this idea I built this app that can be used to check and drill memory of almost all of JavaScript’s built in methods from Object, Array, String, Boolean, Number, and Math objects (approximately 100 methods leaving out the more obscure like Math.asinh() ). Will being able to remember things like the difference between Object.freeze() and Object.seal() actually make my JavaScript any better? I’m not sure but I plan to try drilling for about 15 minutes once or twice a week to find out.

