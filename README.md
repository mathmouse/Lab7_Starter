# Check your understanding

1. Where would you fit your automated tests in your Recipe project development pipeline?

I would fit them within a Github action that runs whenever code is pushed. I think that this allows for better collaboration: other people can actively monitor and help with test failures. This also keeps a backlog of what is going right or wrong with your code. It also ensures that tests always run; people may forget to run tests manually so a Github action is more consistent. 

2. Would you use an end to end test to check if a function is returning the correct output? (yes/no)

No. End to end tests involve emulating user actions from start to finish, not for an individual function. Unit tests would be better in that case.

3. What is the difference between navigation and snapshot mode?

Navigation mode tests the page right after loading, which provides an overall performance metric. Snapshot mode takes a "snapshot" of an already loaded page in its current state, which makes it good for finding accessibility issues.

4. Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

Network dependency tree: Avoid chaining critical requests by reducing the length of chains, reducing the download size of resources, or deferring the download of unnecessary resources to improve page load.

html element does not have a lang attribute: If a page doesn't specify a lang attribute, a screen reader assumes that the page is in the default language that the user chose when setting up the screen reader. If the page isn't actually in the default language, then the screen reader might not announce the page's text correctly.

Render-blocking requests: Requests are blocking the page's initial render, which may delay LCP. Deferring or inlining can move these network requests out of the critical path.



