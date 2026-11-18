## **Analysis of Price Statistics**

All four items experienced **price increases**, ranging from 5.25% to 19.41%.

| Item        | Mean   | Median | Price Change |
| ----------- | ------ | ------ | ------------ |
| Oil B       | 324.83 | 324.00 | +15.28%      |
| Pulse C     | 205.91 | 206.00 | +5.25%       |
| Staple A    | 160.89 | 112.50 | +12.98%      |
| Sweetener D | 576.81 | 167.75 | +19.41%      |

### **Key observations**

1\. **Sweetener D** has the highest percentage increase (19.41%). Its mean (576.81) is also much higher than its median (167.75), suggesting that unusually high prices or outliers are pulling the average upward.

2\. **Oil B** increased by 15.28%. Its mean and median are almost identical, suggesting a relatively balanced price distribution.

3\. **Staple A** increased by 12.98%. Its mean (160.89) is noticeably higher than its median (112.50), suggesting possible high-price outliers.

4\. **Pulse C** experienced the smallest increase (5.25%). Its mean and median are nearly identical, indicating a relatively balanced distribution.

### **Overall conclusion**

**Sweetener D experienced the largest price increase, while Pulse C experienced the smallest.** The large differences between the mean and median for Sweetener D and Staple A suggest possible outliers that should be investigated.

**Important:** The percentage changes measure the difference between average prices on the first and last dates, whereas the mean and median summarize prices across the dataset. Also, a similar mean and median does not necessarily mean prices were stable over time.


Audit Table

Claim: "All four items experienced price increases, ranging from 5.25% to 19.41%."

Color: Green

Reasoning: printed the first and last date prices for each item and worked out the % change myself. All four went up and the range matches.

Accepted

Claim: The table values (mean, median, % change)

Color: Green

Reasoning: compared it with my own stats table. Same numbers.

Accepted

Claim: "Sweetener D has the highest increase (19.41%)... mean much higher than median, suggesting outliers are pulling the average up."

Color: Green for the % change, Amber for the outlier part

Reasoning: 29.5/152 x 100 = 19.41. The gap between mean and median is 409, and I had already flagged the 9999 value in week 2 so this makes sense.

Accepted

Claim: "Oil B... mean and median almost identical, suggesting a balanced distribution."

Color: Amber

Reasoning: gap is only 0.83. A small gap hints the prices are balanced but doesn't fully prove it.

Accepted, with caution

Claim: "Staple A... mean noticeably higher than median, suggesting possible high-price outliers."

Color: Amber

Reasoning: gap is 48.39. In task 3 I removed the 1250 value and the mean dropped to 111.39 while the median stayed 112.5.

Accepted, my task 3 basically proves it

Claim: "Pulse C experienced the smallest increase (5.25%)" and "Pulse C the smallest" in the conclusion

Colour: Green

Reasoning: 10.5/200 x 100 = 5.25 so the number is right. But on the first date Pulse C's City 2 price is missing, so its starting price is just City 1, while the other items average both cities. City 2 was around 6 higher than City 1 for the other items that day, so Pulse C's actual increase might be lower than this.

Number accepted, but comparison rejected since Pulse C's starting price isn't calculated the same way as the rest

Claim: "The percentage changes measure the difference between average prices on the first and last dates."

Color: Red

Reasoning: I never told the AI how I calculated the % change so it guessed. Checked my code and it happened to be right.

Accepted, but it's still talking about something it wasn't shown

Claim: "A similar mean and median does not necessarily mean prices were stable over time."

Colour: Amber

Reasoning: mean and median show the price level overall, not how it moved over time.

Accepted

Something the AI missed are the outliers since they aren't on the first or last date so they don't affect the % change at all, only the mean. It didn't mention that.

CONFUSED CLASSMATE;

I don't get why you're questioning the mean. Staple A has an average price of 160.89, so surely that's its typical price?

The mean uses every price in the dataset, so wouldn't it be more accurate than the median of 112.50?


but every price in the data set isnt necessarily correct. there will be outliers and extremes caused by external factors that drag the mean upwards or downwards


But why does that make the median more representative? Those extreme prices are still part of the dataset, right? Wouldn't ignoring them give us a less accurate picture of the actual prices?


The median doesn’t ignore 1,250. It just doesn’t let one huge number pull the answer up. Most Staple A prices are between 100 and 122, so a typical price should be around there. The median is. The mean is higher than almost every real price. Also, 1,250 was flagged as a possible error, so it shouldn’t fall into the typical caztegory.


Okay, I see why 112.50 might better represent what people usually pay.

But why shouldn't we just remove the suspicious 1,250 price and calculate the mean again? Wouldn't that give us a more accurate typical price than the median?


yea but for now we've only flagged that value. outliers also dont necessarily mean the value that was produced was wrong. which is why median is the better option in a situation like this where u dont need to remove values from the data set


Okay, that makes sense. We can't just delete 1,250 without confirming it's an error, and the median gives us a typical price without being heavily affected by it. But why wouldn't we always use the median instead of the mean, then?


because outliers dont necessarily exist in every dataset so there are cases where the mean works just as well as the mdian as we saw w oil b and pulse c


Okay, but Oil B and Pulse C having similar means and medians doesn't necessarily prove there are no outliers, right?

How would you decide whether the mean or median better represents the typical price in a dataset?


usually u calculate both and compare the 2. if they are nearby we can expect there to be no outliers so either works. if not then rely on median


But why does having a similar mean and median mean there are no outliers? Couldn't a dataset have both very high and very low outliers that cancel each other out, keeping the mean close to the median?




yes true but it acts as the first assessment of the data not the only one. we still analyze max and min values or js the dataset in general


Okay, now I get it! Comparing the mean and median is just an initial check, not definitive proof. We also need to examine the actual price distribution and extreme values.

So for Staple A, 112.50 is a better typical price than 160.89 because the high outlier pulls the mean upward.

You've convinced me!


Reflection

Going back over my first draft, I said more than the data could back up in a few places. In Task 3 I wrote that the median is unaffected by outliers, but it's just less affected and it happened to stay at 112.5 here. In my note I said the 9999 value was probably doing the same to Sweetener D, but I only tested Staple A, so that was a guess. My note also didn't answer whether prices actually went up since I couldn't do the % change on my own, and even after adding it, it only compares the first and last date, and Pulse C's first price only came from City 1 since City 2 was missing. My means and medians also mix both cities and all dates, so they hide any differences between them. In the classmate chat I said outliers come from external factors, which I can't prove, and that a close mean and median means no outliers, which isn't always true since high and low outliers can cancel out. Main thing I learned is that most of what I can say from this data is what the numbers show, not why.
