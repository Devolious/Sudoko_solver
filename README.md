# Sudoko_solver
Sudoku is a logic-based, combinatorial number-placement puzzle. In classic sudoku, the objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid (also called "boxes", "blocks", or "regions") contains all of the digits from 1 to 9. The puzzle setter provides a partially completed grid, which for a well-posed puzzle has a single solution.

**Abstract-**
Sudoko is one of the most famous puzzle games across the globe and people like to train their mind by solving Sudoko puzzle, I too love to solve Sudoko puzzle spending hours sometimes on solving but one problem which I found while solving the sudoko puzzle is it is often tiring to invest lots of hours on it but if at the end of the day I am unable to get the solution to the puzzle, then it becomes quite frustrating. So I thought to use my algorithmic skills to extract the solution at the end of the day, for solving the Sudoko in general Backtracking solution is being used so I coded the entire logic behind the backtracking solution of Sudoko solution and in the due process I got several bugs in my code which I patience-fully handled and made a complete solution to Sudoko puzzle , using this backtracking algorithm I could get the solution of Sudoko puzzles I couldn't solve, But fitting all numbers into the grid was very cumbersome process, I am a Deep Learning enthusiast and have expertise in Computer Vision. So I thought to incorporate Computer vision in my project, I wanted to just upload the photo of the sudoko puzzle in the system and get the output laid on it.
Now I had several problems posed infront of me-
  1-Selection of main grid of Sudoko puzzle.
  2-Extracting the rows and columns lines from Sudoko Puzzle.
  3-Extracting each small block and recognising the digit in it.
  4-Getting solution from Helper function.
  5-Stacking both images of solution and puzzle to get desired output.
  
**Process:-**
1-Preparation of Image and Contour-Mapping-
  Gaussian Blur and Adaptive Thresholding was done on the grayscale image after resizing.The preprocess function can be found in Utils.py and the driver function is Sudoko_main here.Find the contours in the image and for verification we can print them also. Now we need the biggest Contour as this will contain the Sudoko puzzle for this part we first find the four corners of the contour by converting into approximate polygon and compute areas and compare and pick the maximum one.We also use perspective transform here and warp perspective to get perspective of the image even with augmentations.
2- Finding digits by converting image to grids-
   We split image using numpy hboxes and vboxes into 9X9 grid and extract each box. Now for prediction we need a CNN model thus we can prepare a CNN model for digit recognition or can use pretrained model.With the help of the CNN model we set a threshold above which if confidence is present then a certain number is present in the box and it is replaced in the grid.Sudoko_solver is the function for solving the Sudoko puzzle using backtracking.
3-Finally Stacking the images-
   Both the solution image and problem image were added with certain weight such that a mizture of both is seen which gives us an impression that both are stacked.
   
**Conclusion:-**
Currently my model inputs a Sudoko image and stack the solution on it and displays the stacked image.

**Scope of Improvement:-**
 * Live webcam solving feature will be added.
 * Deployment in website will be done.

Thank you and as always ALL SUGGESTIONS ARE WELCOME !! 
