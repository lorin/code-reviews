# Code reviews

Some notes on things to keep in mind during a code review.

## The gist

Can you articulate the problem that the PR addresses?

Can you describe the solution in your own words?

## Tests

Look at the tests first. Can you understand the tests without looking at the code?

## Database changes
Note: this includes not just schema changes, but also changes to data being written to the database.

What happens during deployment when an old and a new version are both running at the same time? 

What happens if this change is rolled back?

## Operational concerns

Do we need additional monitoring (logging, metrics)?

## Robustness

What happens if there are unexpected data inputs?

## Other perspectives

* Readability
* Maintainability
* Testability
* Performance
