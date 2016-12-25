# Jest Test

Running `yarn test` results in the following output:

    yarn test v0.18.1
    $ jest
     PASS  ./test.js
      console
        ✓ logs to the console (1ms)

    Test Suites: 1 passed, 1 total
    Tests:       1 passed, 1 total
    Snapshots:   0 total
    Time:        0.801s, estimated 1s
    Ran all test suites.
    ✨  Done in 1.28s.

We should be `testing console log` pop up somewhere. Updating the jest
configuration in `package.json` to include `"testEnvironment": "node"`
instead of the default `jsdom` results in:

    yarn test v0.18.1
    $ jest
     PASS  ./test.js
      console
        ✓ logs to the console (2ms)

    Test Suites: 1 passed, 1 total
    Tests:       1 passed, 1 total
    Snapshots:   0 total
    Time:        0.367s, estimated 1s
    Ran all test suites.
      console.log test.js:3
        testing console log

    ✨  Done in 0.97s.

This includes the console.log output we'd expect to see.
