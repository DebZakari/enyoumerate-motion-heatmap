# motion-heatmap-opencv
To-Do:
1. Create YOLOv5-zoning repository
2. Remove directional
3. Identify coordinates of each area
4. Each area1, area2, area3, area4, should have counting mechanism
via PointPolygonTest
5. Each area should have a unique count variable (count1, count2, etc.)
6. Saving count variable to csv considering its date and which area (area1, area2, etc.)



Original Logic:
if int(result)>0 [PointPolygonTest] - meaning object is inside the polygon in area1
	then it finds if (id) is in (data)
		then it increments count variable
			after increment, it writes in csv finding its date first, then writing in the row_index+1 which means it writes below the first row - reason for this para dili ma overwrite ang date nga nakabutang daan sa csv


Zoning Logic:
Original logic had result = area1 PolygonTesting. For this zoning logic, we'll use multiple result variables (result1, result2, etc.)
Original logic had only 1 count variable because it only had 1 area to consider. For zoning, we'll use multiple count variables (count1, count2, etc.)

if int(result1)>0 [PointPolygonTest] - meaning object is inside the polygon in area1
	then it finds if (id) is in (data)
		then it increments count1 variable
			after increment, it writes in csv at row_index+1 (which corresponds to area1)

if int(result2)>0 [PointPolygonTest] - meaning object is inside the polygon in area2
	then it finds if (id) is in (data)
		then it increments count2 variable
			after increment, it writes in csv at row_index+2 (which corresponds to area2)

if int(result3)>0 [PointPolygonTest] - meaning object is inside the polygon in area3
	then it finds if (id) is in (data)
		then it increments count3 variable
			after increment, it writes in csv at row_index+3 (which corresponds to area3)

if int(result4)>0 [PointPolygonTest] - meaning object is inside the polygon in area4
	then it finds if (id) is in (data)
		then it increments count4 variable
			after increment, it writes in csv at row_index+4 (which corresponds to area4)


### Steps to run Code
- Clone the repository.
```
https://github.com/DebZakari/enyoumerate-motion-heatmap.git
```
- Goto the cloned folder.
```
cd enyoumerate-motion-heatmap

```
- Upgrade pip with mentioned command below.
```
pip install --upgrade pip
```
- Install requirements with mentioned command below.
```
pip install -r requirements.txt
```
- Run the code with mentioned command below.

 - Run 
 
`python filename.py`


<video src="https://user-images.githubusercontent.com/34125851/220031062-29dd61ed-29b3-4f8a-b15b-b07d934f13fd.mp4
"></video>





### Inference on a video:
https://www.youtube.com/@Pyresearch/videos
