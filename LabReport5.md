# Lab Report 5 - LAST WEEK !!!!
I'm for real going to miss this class and how tight knit and interactive everything waas. I'd like to thank all the staff reading this before getting into my lab report. You guys are the best!!

## How I found the differing results
To run all the tests with the different implementations of `MarkdownParse.java`, I first switched my directory to `group-markdown-parse`. From here, I ran `bash script.sh > results.txt`, which ran all the `test-files` and put the results in a file called results.txt. Then, I switched the directory to `joe-markdown-parse` which contained the joe's implementation, and ran the same command: `bash script.sh > results.txt`. Then, I switched to the directory containing both these directories and ran 'diff group-markdown-parse/results.txt joe-markdown-parse/results.txt` which output the lines that differed between the two `results.txt` files in the terminal. From here, I picked two tests (test-file 201 and , that I thought would be interesting to look into.
## Test 495
Here is my code's output:
![Screen Shot 2022-03-11 at 3 46 25 PM](https://user-images.githubusercontent.com/97696757/157991602-6ed3eb2a-d235-49f7-9861-a760d8f8b195.png)

Here is Joe's code's output:
![Screen Shot 2022-03-11 at 3 46 36 PM](https://user-images.githubusercontent.com/97696757/157991578-8107b311-6101-4518-98bb-50fa7670c6c8.png)

According to [CommonMark](https://spec.commonmark.org/dingus/), Joe's output is correct. The test `[link](foo(and(bar)))` should parse `foo(and(bar))` into a link. 
Taking a look at my code's implementation, I have highlighted what I think is causing this bug below. 
![Screen Shot 2022-03-11 at 3 53 40 PM](https://user-images.githubusercontent.com/97696757/157993163-a708e55e-b210-4411-9bad-5e9d42da8bcb.png)

The code I have checks to see if the input to be parsed has a "." or not. If it does not, it does not end up parsing the input. Removing this condition can allow the code to successfully parse `[link](foo(and(bar)))`.

## Test 12
Here is my code's output:
![Screen Shot 2022-03-11 at 3 57 08 PM](https://user-images.githubusercontent.com/97696757/157993550-929d6bc5-fe6c-4cf7-b26b-8afe1f18699e.png)

Here is Joe's code's output:
![Screen Shot 2022-03-11 at 3 56 56 PM](https://user-images.githubusercontent.com/97696757/157993557-c2e7c72e-ba63-4d29-8147-7fd21a9ea24a.png)

According to [CommonMark](https://spec.commonmark.org/dingus/), Joe's output is correct. The test `\!\"\#\$\%\&\'\(\)\*\+\,\-\.\/\:\;\<\=\>\?\@\[\\\]\^\_\` should not end up parsing, like Joe's code did not. My code did though, it parsed a single character. I have highlighted what I think is causing the bug below.

![Screen Shot 2022-03-11 at 4 04 34 PM](https://user-images.githubusercontent.com/97696757/157993988-1bbc11eb-7923-49db-a220-0a261059c1e3.png)

I believe the bug comes from the code not checking if the closed parenthesis that carry the link is right after the square brackets. The problem with the highlighted code is that it is missing this check. To fix the code, I would add some lines that check if the closed parenthesis comes right after the square brackets. 
