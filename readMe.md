# np.where
- np.where((colSums > 0.8*Size) & (colSums < 1.2*Size) & (colSums == colSumsmax))[1]
- np.where(np.logical_and(colSums > 0.8*Size, colSums < 1.2*Size, colSums == colSumsmax))[1].tolist()

        
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

  # numpy.ma (mask array)
  - Masked arrays are arrays that may have missing or invalid entries.
  - The numpy.ma module provides a nearly work-alike replacement for numpy that supports data arrays with masks.
  - In many circumstances, datasets can be incomplete or tainted by the presence of invalid data. For example, a sensor may have failed to record a data, or recorded an invalid value. The numpy.ma module provides a convenient way to address this issue, by introducing masked arrays.
  - A masked array is the combination of a standard numpy.ndarray and a mask. A mask is either nomask, indicating that no value of the associated array is invalid, or an array of booleans that determines for each element of the associated array whether the value is valid or not.
  - When an element of the mask is False, the corresponding element of the associated array is valid and is said to be unmasked.
  - When an element of the mask is True, the corresponding element of the associated array is said to be masked (invalid).
  - The package ensures that masked entries are not used in computations.
  - As an illustration, let’s consider the following dataset:
   
                import numpy as np
                import numpy.ma as ma
                x = np.array([1, 2, 3, -1, 5])
    - We wish to mark the fourth entry as invalid. The easiest is to create a masked array:

               mx = ma.masked_array(x, mask=[0, 0, 0, 1, 0])
    - We can now compute the mean of the dataset, without taking the invalid data into account:

              mx.mean() --> 2.75

    
