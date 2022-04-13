# kth order statistic from an unsorted array
  - Input: an unsorted array S and an integer k
  - Output: Kth smallest number in S
 
 ## Aprroach
  - For any number v, imagine splitting S into 3 categories
    1. Numbers smaller than v
    2. numbers larger than v
    3. Numbers equal to v
  - Call these S_L, S_R and S_V respectively
  ### Recursion <br>
  ![image](https://user-images.githubusercontent.com/71220864/133939012-0093da4b-7469-49ac-bf97-e81671d60d56.png)<br><br>
  ![image](https://user-images.githubusercontent.com/71220864/133939024-391612d6-f65b-4861-a87d-31ef055491d8.png)<br><br>
  - The effect of the split is thus to shrink S from S to max{|S_L|,|S_R|}
  - To ensure the best splitting of the array, we should choose the median
  - However we do not have that information, and it would be expensive to compute
  - We can choose a number close to the median with the following process

  ### Choosing the pivot
  - Divide the n elements into groups of 5
  - Find the median of each of the n/5 groups
  - Find the median x of the n/5 medians using recursion
  ![image](https://user-images.githubusercontent.com/71220864/133939128-bdf5e035-9079-42ae-8437-05c66549e27b.png)<br><br>
  ### Analysis
  - The recurrence relation comes out to be<br>
  ![image](https://user-images.githubusercontent.com/71220864/133939151-e964d0d5-5857-434c-aceb-92c7319140a0.png)<br><br>
  ![image](https://user-images.githubusercontent.com/71220864/133939186-1466ac33-5496-4bac-8e0d-32a3081c6dc1.png)<br><br>
  ![image](https://user-images.githubusercontent.com/71220864/133939170-86dc65fd-bf91-4b86-935f-2d0db9ded2b2.png)<br><br>
  ![image](https://user-images.githubusercontent.com/71220864/133939193-2e243e35-0748-4488-8b79-8a50137bb481.png)<br><br>

#### Thus we are able to find the kth order statistic in linear time O(n)




  
