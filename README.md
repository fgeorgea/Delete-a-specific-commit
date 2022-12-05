# How to delete a specific commit

## Yes, if you arrived here, you'll have your answer, I know it was a pain in the *ss, but don't worry, here's your answer.

> First, be sure of which commit you want to erase. There won't be any way to get it back, it won't be anywhere.*

1. First, execute :
```
git log --oneline
```    

There you should have the commits just like the screenshot shows down below. You have to identify which commit you want te delete and the **previous one**, this is really important.

2. The, execute this command by replacing 'PREVIOUS_ID' by the id of the previous commit of the commit that you want to delete. In this case it would be '35ff9c6'.
```
git rebase -i PREVIOUS_ID
```

![terminal_screenshot](git_log_screenshot.png)

3. Now, a screen should appear with lots of stuff written in it. Don't worry you only have to change one word. 

    The first line should be :
pick the id of the commit you want to delete then the name of the commit

    The second line should be the same thing but for the previous commit.

    Just like so :

![terminal_screenshot](rebase_rename.png)

4. If you have this, you are almost done, just replace the word "pick" by "drop" in the first line.

    Now save and quit the file, and you are DONE !