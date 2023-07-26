  **TASK 3 ON ADAVANCED FUNCTIONS IN EXCEL**
 
  Learning adavanced function enabled us perform complex calculations and manipulate data effectively.we were taught how to us the vlookup,Hlookup,Xlookup and conditional functions,at the 
  end of the session we were assigned to work on same data set with Task 2.

   **DATA SET(SALES DATA)**

![image](https://github.com/Maris27/TASK-3-3rd-cohort-Data-Analysis-Training-/assets/140453106/862f1fc0-9ba2-49dd-bdf3-da2bab33922f)
  
1.we were asked to calculate the average revenue generated from each sale of a particular product "PASEO"
2.The number of sales made in the Government and midmarket segement
3.The total revenue generated from the sales of "montana" in canada
4.In which country,segment and month was the highest unit of goods sold?
5.what is the total profit made in December.

**DATA MANIPULATION**
1.Responding to this i used the advanced function of average which is AVERAGEIF, with this function i can ascertain then total average sales of specific product as specified in the task.formular used =AVERAGEIF(C2:C701,"PASEO",J2:J701)

2.in calulating the number of sales made in the two segment,i used the countif function with syntax=countif(range,citeria),with this i could get the sales of each of the segment.i worked on the two segments seperatelty before adding up 
Government: =COUNTIF(M2:M701,"GOVERNMENT"). M2:M701 as the range needed,its also the column of segments.Same applies for midmarket.
Midmarket:  =COUNTIF(M2:M701, "MIDMARKET").

3.Used SUMIFS to get the total revenue generated from sales of montana in canada, this is because the sumifs function add values from a range based on a multiple criteria.
syntax:=SUMIFS(sum_range, criteria_range1,criteria1...) you can add more criteria.Therefore to get the total revenue i used the following =SUMIFS(J2:J701, B2:B701,"CANADA",C2:C701,"MONTANA").

4.Firstly i calculated the highest unit of goods sold using the MAX function,max means maximum.=MAX(E2:E701) i used the uni of goods column as athe range which is E2:E701. 
to know the country ,segment and month it was sold i used the VLOOKUP function. The vlookup means vertical lookup, it searches for a value in the left most  column of a table and it returns a related value from a specified column.and it has entered as follows
=vlookup(lookup value,table array,column index num,range lookup).the look up value is the total unit sold in this case,table array is the table you are to search from,remember it has to be the leftmost column of the table,so we had to move the segment and country column to the left side of the column,index number haas to be the columun number you want vlook up to look out,range lookup is usually false to get accurate response. 
C0UNTRY:=VLOOKUP(P7,E2:N701,10,FALSE)
SEGMENT:=VLOOKUP(P7,E2:M701,9,FALSE)
MONTH:==VLOOKUP(P7,E2:M701,8,FALSE)
With the above entries was able to arrive at my answers.


5.I used the sumif function to ascertain the total profit in december because sumif is afunction that add values from a range based on a specific criteria, in this task our criteria was the total profit made in the month December alone.Its as follows 
=SUMIFS(range_ "criteria", sum_range)the range which is the profit column and our criteria is "DECEMBER",sum range is the profit column
=SUMIF(L2:L701,"DECEMBER",K2:K701).

