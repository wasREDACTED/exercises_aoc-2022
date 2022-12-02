<!-- markdownlint-disable MD033 -->
# Day 1 - Calorie Counting for Elves

## Part 1

- *[Image of Shortcut][p1]* [<img src="./part1.png?raw=true?v_DATE" width=25% align=right alt="A screenshot of the macOS Shortcut App, showing the steps described below in the breakdown section.">][p1]

[p1]: ./part1.png

### Usage

1. Select text
2. Choose the shortcut from the services menu

### Breakdown

1. Split text on double newline
2. For each split group
   1. Split by newline
   2. Calculate sum of group
   3. Add sum to dictionary
3. Get the dictionary's maximum value
4. Output the result

<br><br>

## Part 2

- *[Image of Shortcut][p2]* [<img src="./part2.png?raw=true?v_DATE" width=25% align=right alt="A screenshot of the macOS Shortcut App, showing a breakdown of the described steps.">][p2]

[p2]: ./part2.png

### Usage 2

- See Part 1

### Breakdown 2

1. Split text on double newline
2. For each split group
   1. Split by newline
   2. Calculate sum of group
   3. Count characters in Sum
   4. Append `<Count>- <Sum>` to `itemSums`
3. Filter itemSums by Name Desc with a 3 item limit
4. Cleanup count with regex
5. Sum the top three
6. Output the result

> **Warning**
> The character count is pretty lax method to get around the name sort not accounting for numerical value.
>
>- *See [Take 2 for Part 2](part2Take2.png)*  
> In Take 2, JavaScript is executed via
>   + an encoded URL and
>   + "Get contents of webpage at URL"
>
>   ```html
>   <script>
>     var rawText = `itemSumsText`
>     var needToSort = rawText.split("\n");
>     var sorted = needToSort.sort((a, b) => a - b );
>     document.write(sorted.reverse().slice(0,3).join("<br>"));
>   </script>
>   ```
