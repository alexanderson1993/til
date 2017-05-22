# Pre/Post Scripts

NPM is a cleverly powerful tool. One thing that is less than obvious is the `run-scripts` or `run` command. With it, you can define customs scripts to run in your `package.json` file, and then run them from the command line with a simple `npm run **command here**`

Even less known is the `pre-` and `post-` script commands. These are commands which are executed before and/or after another command. For example, you can put this in to bundle your code before deploying it to NPM:

```
#package.json
{
...
  "scripts":{
    "prepublish":"gulp build"
  }
...
}
```

Then, anytime you run `npm publish`, your code will automatically be compiled.

Finally, you can put `pre-` and `post-` scripts on any command, by just prepending the command's name in `package.json`:

```
#package.json
{
...
  "scripts":{
    "pretest":"gulp build", // Make sure my tests can run on bundled code
    "test":"./bin/tests"
  }
...
}
```

Now I don't have to worry about building my code for tests either!
