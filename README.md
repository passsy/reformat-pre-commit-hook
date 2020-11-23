# reformat-pre-commit-hook

A git `pre-commit` hook template which runs checks on staged files only.

The [git pre-commit hook] is a great way to automate code-formatting and check `lint` beforehand, preventing you from committing error or malformatted code.
But hooks don't differentiate between staged and unstaged files.
This causes problems such as preventing the commit of a documentation change because a source file (unstaged) has an error.

This pre-commit hook template stashes all unstaged files before running the pre-commit hook tasks, leaving the repo in the exact state it would be with the commit.
After the tasks ran (in success or erro), all files will be unstaged again and `git` can continue with the commit.


## License

```
Copyright 2020 Pascal Welsch

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```