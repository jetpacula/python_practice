#script below creates n*n matrix by spirally filling cells from 1 to n^n in the center
#try and run it by yourself!

a=int(input())
row=0
col=0
count=1
A=[[0 for x in range(a)]for y in range(a)] # create empty n*n matrix
up=False
left=False
x=True
b=a-1
Mvhor=1
Mvver=1
tempx=a
tempy=b
for rows in A: # for each row in matrix go one by one to fill rows
    for cols in rows: # for each cell in row fill each cell one by one
        if x and not left and tempx!=0: 
            A[row][col]=count #fill cell with current n value
            count+=1 #increment cell value for next input
            col+=1 #move to next column
            tempx-=1 # decrement temp var until it reaches zero, then change direction
            if tempx==0: # changing direction if var reaches zero
                col-=1# move current cell coordinates back to one column, because it should be outside the matrix size
                row+=1 #move one row down
                x=not x # change direction to Y axis
                left=not left # move right next time we go horizontal again
                a-=1
                tempy=b
                
                 
                continue
                
        if not x and not up and tempy!=0: #condition to move vertically and down
            A[row] [col] = count
            
            count+=1
            row+=1
            tempy-=1
            
            if tempy==0:
                b-=1
                col-=1
                row-=1
                x=not x
                up=not up
                tempx=a
                
                continue
        if x and left and tempx!=0: # condition to move left by x axis
            A[row] [col] =count 
            count+=1
            col-=1
            tempx-=1
            if tempx==0:
                row-=1
                col+=1
                x=not x
                left=not left
                tempy=b
                a-=1
                
                continue
        if not x and up and tempy!=0:
            A[row] [col] =count
            count+=1
            row-=1
            tempy-=1
            if tempy==0:
                row+=1
                col+=1
                b-=1
                x=not x
                up=not up
                tempx=a
                
                continue

for line in A: # print results!
    print(*line)

                
            
