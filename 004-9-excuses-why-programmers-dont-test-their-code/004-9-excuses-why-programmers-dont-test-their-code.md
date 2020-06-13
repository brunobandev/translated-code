Written by **Daan** - [original version](https://medium.com/better-programming/9-excuses-why-programmers-dont-test-their-code-8860a616b1b5)

Translated and adapted by [**Bruno Bandeira**](https://github.com/brunobandev/translated-code)

# 9 Excuses Why Programmers Don’t Test Their Code
A list of excuses we can all relate to

![alt text](004-files/001.jpeg "Code Testing")

Programmers and testing — it definitely isn’t a match made in heaven. Although most programmers understand the importance of testing and why it’s useful, sometimes we just don’t feel like it.

There are plenty of excuses that get used all the time just to avoid one thing: writing tests.

Have you ever used any of the excuses on this list?

## 1. "My Code Works Fine — Why Should I Even Bother Testing It?"
This kind of statement is often made by cocky developers. Thinking one could write perfect code is naive, at best. Even the best programmers make mistakes. And they make them all the time.

Nobody is perfect — mistakes happen way more often than they should, and that actually is totally fine since we learn from these mistakes.

It’s OK to be confident about your code. But even if another developer reviewed your code and approved it, you shouldn’t be satisfied … yet. Even if you’ve manually tested some use cases. there’s still a danger in all of these things.

All of these things rely on the human factor. And that’s exactly what you shouldn’t want since the human factor fails from time to time. When that happens you want to have proper tests that have you covered.

> "Nobody actually creates perfect code the first time around, except me. But there’s only one of me." Linus Torvalds

## 2. "This Piece of Code Is Untestable"
What you mean is you don’t really know how to test that piece of code. Chances are your code is structured in a bad way, which makes it untestable. If it’s just that one piece of code, refactor it into small and testable pieces.

When you’re dealing with code that really is untestable since it’s poorly designed and the code is suboptimal, you’ve got some bigger problems. Untestable code is expensive to maintain and modify. On top of that, untestable code will be difficult for new team members to learn.

If you’re not testing your code, you’ll eventually run into the problem where developers lack the confidence to deploy the code. The lack of testing makes them anxious since they don’t have the confirmation that their changes didn’t break anything.

## "I Don’t Know What to Test"
Are you in doubt about what to test? Test it all!

A great start would be to test the most common case of everything you can. This will tell you when that part of the code breaks, which has the most impact.

But there’s more to testing than just clicking through the happy-path scenario. You should test some edge cases of parts of your code that are the most complex or pieces of code that are most likely to have errors.

Whenever you find a bug, it’s considered good practice to write a new test that covers that test case.

Make writing tests part of your routine — don’t make it optional.

## 4. "Testing Increases the Development Time, and We’re Running Out of Time"

This is one of the biggest misconceptions when it comes to testing. Whenever you start writing tests for the first time, it definitely increases development time. At first, you need to learn how to write testable code and how to make proper tests. This is an investment that you make for the long run.

Once testing becomes a habit, it’ll save you plenty of time. And headaches. Having tests will save you the problem of developers that lack the confidence to deploy their code — despite the fact that you have the ability to run your entire test suite at the ease of clicking a button, of course.

## 5. "The Requirements Are No Good"
Bad requirements are not an excuse to skip writing tests. You’ve got plenty of options to figure out the requirements. Sometimes it gets even worse. Sadly enough, undocumented requirements are a reality that most of us face more often than we’d like.

In both cases, you have to work with whatever little piece of documentation you can get your hands on. Try digging through old emails or some notes that you’ve made to try and find some clues.

You also want to take a look at the current or older versions of the application — if that’s possible, of course. You’ll probably find a lot of hidden clues here. Don’t forget to take a look at the tests. They might be full of hidden gems that could help you out.

Last but not least, try talking with some team members. They might know much more about the undocumented requirements you’re looking for. Think about that one thing that got discussed, but not documented, in that one meeting that you couldn’t attend.

## 6. "This Piece of Code Doesn’t Change"
"There’s no point in testing code that doesn’t change. That’s a complete waste of time."

Well, the only certainty we have in software development is the requirements will change. Sometimes they seem to be ever-changing.

People change their minds for many reasons and they do so on a regular basis. Changing requirements can be caused by many things. Some people request a feature, but they don’t actually know what they want. Unfortunately, this happens a lot. Another reason requirements might change is because of politics within an organization.

Whenever you’re dealing with changing requirements, you should prioritize testing the most common flows.

## 7. "I Can Test This Way Faster If I do It Manually"
The problem with manual tests is you have to do them over and over again. And again.

Yes, you might test a certain feature faster when you do it manually once. But manual tests are very time consuming when you have to do them over and over again. Manual testing is endless and very expensive.

Writing tests takes some time, but once you’ve got your test, you can run it infinite times, and it only costs a fraction of the time compared to manual testing. Running an automated test takes less time than opening up your browser and typing in the address of the page.

## 8. "The Client Only Wants to Pay for Deliverables" 
Every client wants to see as many deliverables as possible since that gives them the feeling the development team is doing some actual work. When possible, they want to keep the costs as low as possible.

This is exactly what developers tell their managers whenever they don’t feel like testing.

Tests are an essential part of software development, and this part of the code is just as important as any other piece of code — so you should treat it like that. Include time to write tests in the estimates that you make.

Writing tests reduces maintenance costs and lowers development costs in the long run.

## 9. "This Piece of Code Is So Small … It Won’t Break Anything"
Every developer has written pieces of code that are so small that they couldn’t possibly break anything major. And yet, it still managed to break something. That two lines of code that you’ve added managed to break something that you didn’t foresee.

How do you know your code works perfectly?

Please, let your words be backed by some actual tests. Thorough testing filters out critical bugs, ensuring the code works the way it’s intended.

## Wrapping It Up
Could you relate to any of the excuses on this list?

I guess we’ve all used one of these before. Next time, we probably should just consider writing the tests since we all know not testing our code will come back to bite us at some later point.

Thanks for reading!