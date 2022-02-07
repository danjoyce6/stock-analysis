# VBA ---
## Project Overview ---
The purpose of this analysis was to refactor the working code from the Module 2 solution code of Stocks Analysis to only loop through the data once instead of twice and analyze the performance of the stocks in the Excel Workbook with data on green energy stocks from the years 2017 and 2018.  The Excel Workbook contained data on ceratin green energy stocks that Steve was analyzing for his parents to measure the performance of the stock that they invested in.  The initial investment that Steves parents made was in the company stock DQ.  This companies stock had performed poorly.  The analysis that was run performed calculations to produce data on the 'Total Daily Volume' and 'Return' on investment based on the starting and ending price of the stocks.   A starter code was supplied and code was added to refactor the code to only loop one time instead of two times.  One of the goals of the project was to determine whether refactoring code made in improvement in the run time of the VBA script.  Although DQ performed poorly in 2018, it performed well in 2017. ---
## Results ---
### Execution Time and Code Analysis ---
Refactoring the code decreased the execution time on both years 2017 and 2018 in the Excel Workbook.  For the years 2017 and 2018, the unfactored code executed in 3.238281 and 3.292969 seconds, respectively.  However after refactoring the code for years 2017 and 2018, the macro's were executed in 0.1210938 and 0.1328125 seconds.  This marks a large decrease in the exeuction time that can be attributed to the refactoring of the code from the original. ---

![VBA_Challenge_2017](https://user-images.githubusercontent.com/88444529/132959490-40ad5357-9640-4005-ba00-466f32496adc.PNG)
![VBA_Challenge_2018](https://user-images.githubusercontent.com/88444529/132959497-d0ab0714-d6b6-4027-b0ee-4d1b6c5fb5e7.PNG) ---
![VBA_Challenge_2017_Raw](https://user-images.githubusercontent.com/88444529/132959500-cffe7259-8a51-4a91-9efa-c7a901a8ea81.PNG)
![VBA_Challenge_2018_Raw](https://user-images.githubusercontent.com/88444529/132959504-a53e515b-1eec-43e9-945b-4d0c3bc3db8c.PNG) ---

This decrease in time can be attributed to only looping through the data one time in the refactored code, rather than looping through all of the data two times in the unfactored code.  At the end of the loop the tickerindex variable was increased, and the loop continued,  In the original code, there was no tickerindex variable to reference as the index.  In the original code, it had to loop through all of the tickers and set each total volume to 0, then loop through the year analysis code, before returning the totalvolume, ending price, and starting price.  As seen in the code, by initializing the tickerindex variable to 0 and then referencing that variable as the index, only one loop was necessary.  The tickerindex was used as the index variable to include the ticker name as well as make the calculations on the years worksheets to find the starting and ending price before increasing the tickerindex to the next stock and finally closing the loop.  This did not change the functionality of the code, but it made it more efficient by improving the logic and making the code take less steps. ---
--- ![VBA_Code_Raw_1](https://user-images.githubusercontent.com/88444529/132959514-f410bae4-15d7-48f0-a012-06745fbaadb9.PNG)
![VBA_Code_Refactored_1](https://user-images.githubusercontent.com/88444529/132959521-ba6e0239-a071-48ec-9f70-06746390fd89.PNG)
![VBA_Code_Refactored_2](https://user-images.githubusercontent.com/88444529/132959523-2e31fdbc-2e4e-411f-8aed-65437a936774.PNG) ---
### Stocks Analysis ---
Out of the 12 stocks analyzed in 2017, all of them had a positive return except for TERP which decreased by 7.2%.  The best performing stock was DQ with a 199.4% return, which is the stock that Steve's parents invested in.  The total daily volume was the highest for FSLR with 684,181,400 and had a 101.3% return during the 2017 year.  In 2018 only two out fo the 12 stocks analyzed had a positive return.  ENPH and RUN were the only two with a positive return in 2018 of 81.9% and 84.0%, respectively.  Both of those stocks also saw an increase in their total volume.  The stock that Steve's parents invested in DQ, saw a large increase in its total daily volume from 2017 to 2018, but experienced the lowest return of all stocks in 2018 of -62.6% return.  ---
## Summary ---
Refactoring the code provides certain advantages.  Refactoring the code can improve the readability of the code as well as the performance.  Refactoring the code can reduce the complexity of code allowing for better readability.  The performance can also benefit from refactoring.  Original code can include steps that can be truncated or improved upon so that execution is faster.  Another advantage of refactoring code is increasing the knowledge base of the coder.  A disadvantage of refactoring could be the time spent doing it or actually decreasing the functionality of the code. ---
The pros of refactoring this code were evident.  The refactored code increased the performance of the code dramatically by significantly reducing the execution time of the code.  The refactored code also improved the readability of the code which improves the user experience.  In regard to cons, it was slightly time consuming but the improvements in performance and readability far outweight any cons.
