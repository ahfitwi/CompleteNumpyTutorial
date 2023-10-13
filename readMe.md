# np.where
- np.where((colSums > 0.8*xhSize) & (colSums < 1.2*xhSize) & (colSums == colSumsmax))[1]
- np.where(np.logical_and(colSums > 0.8*xhSize, colSums < 1.2*xhSize, colSums == colSumsmax))[1].tolist()

        
        Code #1:
        # Python program explaining 
        # where() function 
        
        import numpy as np 
        
        np.where([[True, False], [True, True]], 
        		[[1, 2], [3, 4]], [[5, 6], [7, 8]])

        Output :
                array([[1, 6],
                       [3, 4]])


        Code #2:

        # Python program explaining  
        # where() function  
          
        import numpy as np 
          
        # a is an array of integers. 
        a = np.array([[1, 2, 3], [4, 5, 6]]) 
          
        print(a) 
          
        print ('Indices of elements <4') 
          
        b = np.where(a<4) 
        print(b) 
          
        print("Elements which are <4") 
        print(a[b]) 
        Output :
              [[1 2 3]
               [4 5 6]]
              
              Indices of elements <4
              (array([0, 0, 0], dtype=int64), array([0, 1, 2], dtype=int64))
              
              Elements which are <4
              array([1, 2, 3])
