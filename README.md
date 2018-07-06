# Testing Part 1

## Overview

Take the quiz below to make sure you're familiar with the testing and access modifier lessons covered in this section.

???

# Quiz - Testing Part 1

?: What are benefits of robust test coverage? (select all that apply)

[X] Saves time as application grows
[X] Identifies breaking changes earlier on in developer cycle
[X] Gives confidence to developers that their changes work
[X] Serves as useful documentation
[ ] Slows down development cycle

?: All of the below are types of tests. Select the 2 that are the main two classifications of tests:

[ ] Acceptance
[X] Unit
[ ] UI
[X] Integration
[ ] End to End (E2E)

?: Which of these test types is the quickest:

( ) Acceptance
(X) Unit
( ) UI
( ) Integration
( ) End to End (E2E)

?: Which of these test types provides covers more parts of an application?

( ) Unit
(X) Integration

?: Where does rspec test suite configuration live?

( ) In the test files themselves
(X) In the spec_helper.rb
( ) In the application files

?: What rspec methods take a descriptive string as their first argument? (select all that apply)

[X] `it`
[X] `describe`
[ ] `expect`
[X] `context`

?: How many test examples are in this snippet?

```ruby
Rspec.describe Kitty do
  let(:kitty_cat) { Kitty.new("Franklin", "tuxedo") }

  context "purs" do
    before { kitty_cat.give_milk }

    it "when belly is rubbed"
    it "when fed"
    it "when litter is cleaned"
  end

  it "has whiskers"

  context "meows" do
    let(:kitty_cat) { Kitty.new("Jojo", "tortoiseshell") }

    it "when wants to outside"
    it "when wants to be fed"
    it "for no reason"
  end
end
```

( ) 2
(X) 7
( ) 12
( ) 3
( ) 9

?: In the last example, as the code stands now, how many times will `Kitty#give_milk` be called?

( ) 0
( ) 1
(X) 3
( ) 6
( ) 7

?: In the last examplee, as the code stands now, which instance of `kitty_cat` receives milk?

( ) Neither
(X) Franklin
( ) Jojo
( ) Both

?: In the last example, as the code stands now, how many of each Kitty is created?

( ) 0 kitties are created
( ) 3 Franklins and 3 Jojos
( ) 4 Franklins and 3 Jojos
( ) 0 Franklins and 3 Jojos
(X) 3 Franklins and 0 Jojos

?: Which are valid arguments to `rspec`'s `before` helper method? (select all that apply)

[X] `:each`
[ ] `before` does not take an argument
[ ] `:after`
[X] `:suite`

?: What is the difference between `let` and `let!` for any given test example?

(X) `let` lazily runs the code in its block while `let!` always runs the code in its block.
( ) `let!` lazily runs the code in its block while `let` always runs the code in its block.
( ) There is no difference between these methods, it is just a stylistic choice.

?: How could the `Kitty` spec be improved? (select all that apply)

[ ] Remove tests
[X] Explicitly move logic inside `before` directly into examples that require it
[X] Explicitly move `Kitty` creation directly in examples that require it instead of using `let`s
[ ] Create more kitties

?: What level of code access should be the most thoroughly tested?

( ) `protected`
( ) `private`
(X) `public`

?: When is it alright to leave a method with `public` accessibility when it is not invoked anywhere outside of the class?

( ) To make testing easier
( ) When the class is so small it doesn't matter
(X) No reason to not make method `private`
( ) When the class is not getting tested

???
