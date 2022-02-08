# Week 4 Lab Report
---
## Code Change No.1
<img width="1272" alt="Screen Shot 2022-02-07 at 3 33 44 PM" src="https://user-images.githubusercontent.com/97696757/152890017-67ffec1b-7f34-44af-bc42-b475d013221f.png">

### [Link to Failure Inducing Input](https://github.com/akh1lbokka/markdown-parse/blob/main/edge1.md)

### Symptom of Failure Inducing input:
<img width="1080" alt="Screen Shot 2022-02-07 at 3 24 19 PM" src="https://user-images.githubusercontent.com/97696757/152890443-d710b67e-e140-4d29-ab46-10bdf493efb4.png">

### Relationship Between Bug, Symptom, and Failure-Inducing Input:
The bug here is that the code does not check to see if the `(` immediately follows the `[link]`. This causes the program to get the string inside any parenthesis after the `[]`. In this test case, the code grabs a random string of code that is not meant to be a link, but is however enclosed within parenthesis. 

## Code Change No.2
<img width="1270" alt="Screen Shot 2022-02-08 at 6 21 21 AM" src="https://user-images.githubusercontent.com/97696757/153005912-66265d8f-5267-4d8d-8c5e-457b795978c0.png">

### [Link to Failure Inducing Input](https://github.com/akh1lbokka/markdown-parse/blob/main/edge2.md)

### Symptom of Failure Inducing input:
<img width="954" alt="Screen Shot 2022-02-07 at 3 47 01 PM" src="https://user-images.githubusercontent.com/97696757/152891687-7edd9c53-9676-4313-8ad9-c5757032e678.png">

### Relationship Between Bug, Symptom, and Failure-Inducing Input:
The bug here is that the code does not check to see whether there is an open square bracket for the closed square bracket. The test case here does not have an open square bracket. This is turn can cause the code to try parsing incomplete codes for links, which will cause exceptions. More specifically, `StringIndexOutOfBoundsException`.

## Code Change No.3
<img width="1270" alt="Screen Shot 2022-02-07 at 4 04 18 PM" src="https://user-images.githubusercontent.com/97696757/152892667-ef0cba4c-4ea9-4569-860c-407f2aeb7498.png">

### [Link to Failure Inducing Input](https://github.com/akh1lbokka/markdown-parse/blob/main/edge3.md)

### Symptom of Failure Inducing input:
<img width="986" alt="Screen Shot 2022-02-07 at 3 58 30 PM" src="https://user-images.githubusercontent.com/97696757/152892689-9ca00648-65d1-4688-92bf-f470c7dec06d.png">

### Relationship Between Bug, Symptom, and Failure-Inducing Input:
The bug here is similar to edge case 2, the test does not have a closed parenthesis after the url. The code does not check if there is a close parethesis after the linkurl. Therefore, the close parenthesis index is set to -1. This causes a `StringIndexOutOfBoundsException` to be thrown. 
