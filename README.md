# Code reviews

Some notes on things to keep in mind during a code review.

## Understanding the PR

### The gist

Can you articulate the problem that the PR addresses?

Could you explain the solution, in your own words, to someone else?


### Tests

Look at the tests first. Can you understand the tests without looking at the code?

## Where to focus feedback

### Overall approach

Is the overall implementation strategy sound? If not, what's wrong with it?

### Unhandled cases and failure modes

"What if X happens?"

### Naming

Naming is hard, and hard to change. PR is a good time to provide feedback on that.

### Missing context

For example, what functions do should be clear from their signature (a reader generally should not need to read
the entire implementation to understand what the function does). If it's not clear, provide feedback on how to
add comments to the signature declaration to clarify.

## What not to focus on

### I wouldn't have done it that way

People code in different styles. Unless you find a flaw in the code, "I would have done it differently" is not useful feedback. People do things differently. It's not a good use of time.

### Trivialities

Things that aren't even worth bringing up. 

- unused imports

## In the middle: spidey-sense tingling

Some things may trip your radar, even if you can't explicitly articulate then. 

## Things to keep in mind

### Database impact 

### Changes

Note: this includes not just schema changes, but also changes to data being written to the database.

What happens during deployment when an old and a new version are both running at the same time? 

What happens if this change is rolled back?

### Load

Will this increase the load on the database or change behavior in some other way (e.g., creating
many more rows, increased locking).

### Operational concerns

Do we need additional monitoring (logging, metrics)?

### Robustness

What happens if there are unexpected data inputs?

## Other perspectives

* Readability
* Maintainability
* Testability
* Performance





