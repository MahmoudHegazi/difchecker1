# difchecker1

this repo try to study and anlsysis right diffrent and reach it logicaly without read previous techniques

![image](https://github.com/MahmoudHegazi/difchecker1/assets/55125302/6fd6c79b-66dd-4b09-8908-aa7f121437f3)


ex2
![image](https://github.com/MahmoudHegazi/difchecker1/assets/55125302/9dc4362b-5cc3-4815-b304-b7afdf472ab8)


rule2 (the right algo (max range) ) :

note max range means i used for example from left only 1 number so check with 1 v 1, or used 2 so check with 2 v 2 in programing the length of numbers used or index of last number on left used

![image](https://github.com/MahmoudHegazi/difchecker1/assets/55125302/e451d742-eb6d-4255-b713-810ba2b7a5fa)


confirm again

![image](https://github.com/MahmoudHegazi/difchecker1/assets/55125302/db5c2f27-67ef-4cdc-a7f4-4a46aaebe0a0)


all things contains in max range and last stop and performance solution, performance here means not repeat same check in next ranges

# notes:

* performance only means not repeat same check in next ranges, eg range 1 i check 6 == 6, so when go to next range 2 which have 6 and 3 not repeat 6 == 3 no start with 3 == 3 , if it was not 3 eg 4 so next will be 6 == 6
if hard ignore performance and repeat check of first index within all ranges, all preduoce same result

# what is last index how it works:

![image](https://github.com/MahmoudHegazi/difchecker1/assets/55125302/0752fed5-3f9b-46fd-a17e-0b20685fe9d3)

consider this image, as code show there are 2 cases which reflect 2 if statment

* first case if the number on left which is current number of orignal loop which for example here the number 4 is found true which mean not changed so last index will start from index after the equal of it in this case start from 2

* second case if the number on left deleted and the detection or equal happend in second if (ranges if)
so last range will be same number stoped on it , why becuse next loop will take that number so you can progrmatily reach it
for example in that image case  number 3 , the deletion detected in max range 2 when 2 == 2 so i left the last index same as index of number 2, so when next loop come will be 2 == 2 and use continue



! note this algo for now worked with delete  it right now also have detect the add within it's steps but i not reach it logicaly so let's say it allow us to get 2 things only what deleted and what not changed

what added included in last index steps and within algo but i not focused on it so right now use for detect only deleted and not changed.


!other note I tried this algo with small numbers and tested 4 times it worked in the 4 times and reach answer logicaly so even if not worked with other sanerio the question would be why it worked 4 times logicaly and not worked with other sanerios?



### max range

in other words max range is the slice of right side

example

i loop of left side notes not real code but preperareion when write if will be more clear
``` javascript
[1,2,3], [2,3,1]

[1,2,3].forEach( (litem, i)=>{
   const maxRange = [2,3,1].slice(i-1, i);
   // note previous const always result in 1 item, next check will take all items after current litem to get the next ranges here max range will be more items
0
 
[1,2,3].slice(i+1).forEach( (nextlItem, ni)=>{
  //const maxrange = [2,3,1].slice(laststopedindex,ni+1);
   // here ni+1 is what means of max range which means you allow to check from right side until this part only
});
1
  
});
```
