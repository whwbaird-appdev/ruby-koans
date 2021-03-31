# Ruby Koans

We're going to do [The Ruby Koans](http://rubykoans.com/) (principally written by [@jimweirich](http://twitter.com/jimweirich)) in order to deepen our understanding of the Ruby language, and of the Ruby community's culture (spoiler: it's very quirky). Welcome!

## Getting started

Run the command:

```
ruby path_to_enlightenment.rb
```

You should see output like this:

```
AboutAsserts#test_assert_truth has damaged your karma.

The Master says:
  You have not yet reached enlightenment.

The answers you seek...
  Failed assertion.

Please meditate on the following code:
  /Users/raghubetina/code/appdev-projects/ruby-koans/about_asserts.rb:10:in `test_assert_truth'

mountains are merely mountains
your path thus far [X_________________________________________________] 0/278 (0%)
```

What just happened? The important bits:

 - `ruby path_to_enlightenment.rb`: The equivalent of `rails grade`; both are wrappers around an underlying command to run an automated test suite.
 - `Failed assertion.`: The test failure message.
 - `/Users/raghubetina/code/appdev-projects/ruby-koans/about_asserts.rb:10:in 'test_assert_truth'`: The file and line number of the test that failed.

Let's go to that file, `about_asserts.rb`, and check out Line 10.

```ruby
# We shall contemplate truth by testing reality, via asserts.
def test_assert_truth
  assert false                # This should be true
end
```

Every method whose name begins with `test_` is one **automated test**. Usually, the rest of the method's name should describe what aspect of the program is being tested.

Our job is to make the **assertions** within pass. In this project, the name of the method and comments within will provide guidance. In this case, change `false` to true, and then run `ruby path_to_enlightenment.rb` again. This test will pass, and next we'll be sent to Line 16. Keep going.

## Process

To figure out how to make the tests pass, a few tips:

 1. Try to remember your prior Ruby knowledge, but don't be alarmed if you don't know the answer. A lot of the material in the koans will be new to you — I learned many new things as I was preparing this assignment.
 2. If you don't remember or don't know, take a moment and try to reason it out. Can you guess what the expected value should be?
 3. Look at the name of the test/method — what is under test?
 4. Open a terminal tab, launch `irb` to try out the Ruby expression that the assertion is being made about. You can see what the expected value is in `irb`.
 5. Or, you can simply run the test and see what the expected value is in the test failure message.
 6. Puzzled about why it is what it is? In AppDev I, I encouraged you not to Google, since info on the internet can be misleading for beginners. Now, it's time for you to start developing your Google Fu — go ahead and Google.
    - Just Googling some relevant keywords is a good thing to try. Another good thing to try, in addition, is scoping the search to rubyweekly.com. For example,
      - [https://www.google.com/search?q=ruby+break+statement](https://www.google.com/search?q=ruby+break+statement)
      - [https://www.google.com/search?q=site%3Arubyweekly.com+break+statement](https://www.google.com/search?q=site%3Arubyweekly.com+break+statement)
 7. [The official Ruby docs](https://ruby-doc.org/core-3.0.0/#class-index) might be useful; for example, I needed to look up [what happens](https://ruby-doc.org/core-3.0.0/String.html#method-i-5B-5D) when you provide a `Regexp` as the argument to `String#[]`, which I didn't know you could do. (Answer: it returns the first matching substring, or returns `nil` if there are none.)
 8. As always, ask lots of questions on Piazza.

## Housekeeping

### Clear terminal

After each koan, remember to <kbd>Cmd</kbd>`+`<kbd>`K`</kbd> (Mac) or <kbd>Ctrl</kbd>`+`<kbd>`K`</kbd> (Windows) to clear your terminal.

### Git commits

I recommend also making a Git commit after each successful koan. We don't have our handy web `/git` interface here, so you'll have to do it the old-fashioned way, from the command-line. To make a commit:

```
git add -A; git commit -m "Completed koan"
```

(You can change the message inside the quotations to whatever you like each time.)

### Up-arrow to scroll through command-line history

Remember to use your up and down arrows to scroll through your command-line and `irb` history, rather than retyping things.

## Objectives

With the koans, we're going to learn by seeing and doing. Primarily, our objectives are:

 - Become familiar with how automated tests are written — soon, you're going to have to write them yourself. So, pay attention to how they look.
 - Practice reading other people's code.
 - Expand our vocabulary of Ruby classes and methods.
 - Deepen our understanding of Ruby and Ruby idiom.
 - I want you to at least encounter all or most of the Ruby constructs that you are going to see in Rails from now on, even if you won't be writing them yourself.
 - Some day, you'll have a use case for one of these techniques, and hopefully having seen it, it will ring a bell. It should open up possibilities that you might previously not thought of.

## Work in groups

Consider working in groups, and come to open office hours! It helps to talk things through.

## Don't get hung up

Some of the "THINK ABOUT IT"s in the Koans are really subtle and, to be honest, don't really come up often in the day-to-day of application development. Ruby developers with five years of experience would struggle to guess some of them (I sure did). Don't get hung up on any single thing for too long; make a note to discuss it in class and just keep moving!

## Ask for help

If you'd like hints on any of the projects, like `triangle.rb` or `about_scoring_project,rb`, just ask!
