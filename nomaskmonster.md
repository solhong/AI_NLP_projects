# [NOMASK MONSTER](https://nomaskmonsterupdated.bubbleapps.io/)
NOMASK MONSTER service presents a fun experience to children who are uncomfortable in wearing a mask.
I used [Face Mask Detection API](https://ainize.ai/woomurf/FaceMaskDetection?branch=master), AI that detects whether a mask is worn or not.

# Problem definition and solution
Due to COVID-19, I have seen the news that parents with young children are having a hard time getting their children to wear masks properly. As a solution to children who refuse to wear a mask, I suggest wearing a mask as a winning 'NO MASK MONSTER' in everyday life.
By visualizing the invisible 'coronavirus' in the form of a 'monster', I designed it so that you can experience that you can defeat the monster (coronavirus) if you ar the mask correctly.

While I was thinking about what kind of monster to draw the coronavirus, I suddenly wondered, 
>'What would it look like if children expressed the coronavirus as a monster?' 

So, I asked my cousin, who is an elementary school student, to imagine what it would be like to express the coronavirus as a monster and draw it myself, and the following monster came out. This monster has the ability to prevent children from wearing a mask, so I named it 'NOMASK MONSTER'.

![image](https://user-images.githubusercontent.com/89971178/131846382-e50a18c9-ad39-4f73-b741-b642050c41bd.png)


# UIUX Design
UI was designed using Sketch and Figma, and User Flow and UIUX were designed as follows. 

![image](https://user-images.githubusercontent.com/89971178/131847335-6b4c32b4-67a8-4ebd-82cc-c935cc2ac648.png)

Since the service was for children, the entire design tone was composed of child-like drawings and handwriting.

![image](https://user-images.githubusercontent.com/89971178/131847355-ce9fdcc4-a34e-4755-877e-bcf493bc5d68.png)


# How to implement
1. After designing the UI using Sketch and Figma, I imported the Figma file to Bubble and connected the Face Mask Detection API in Bubble to Ainize as follows. I set the data type as **JSON** because I needed to extract a value that depends on whether the image has mask or not from the JSON key value.

![image](https://user-images.githubusercontent.com/89971178/131847430-147a8a15-d0ea-48ac-b575-3fbd6a364522.png)

2. In Bubble, through Workflow Edit, I set which elements should be displayed according to the flow order of the screen and the result of the API.

![image](https://user-images.githubusercontent.com/89971178/131847514-cf4b6450-eb17-4606-b2f4-c543523a5570.png)

3.Following response indicates whether the image has a mask or not:

(1) If the preceding number 1 appears, the image without a mask has been recognized:    
`<[[1, 0.9999951124191284, 105, 125, 320, 408]]>` 

(2) If the preceding number comes out 0, the image with a mask on has been recognized:   
`<[[0, 0.9999874830245972, 48, 31, 147, 162]]>`

The following regular expression (Regex Pattern) was used to extract the number 1 or 0:    
- Regex Pattern: `<[0-1](?=,)>`

It is possible to extract the number before the ,(comma) among the numbers 0 and 1 in [ ] (brackets) shown in (1) and (2) above. 
I used [Regular expression tester](https://regexr.com/) that can test and find regular expressions that I need.

(1) If the first item is '1' before the extracted comma, the message 'You Lose' is displayed because the mask is not worn or worn incorrectly,

![image](https://user-images.githubusercontent.com/89971178/131848188-a9a3f671-fdec-4a7a-bd6c-6c74bf116883.png)

(2) If the number 0 or 1 is '0' in front of the extracted comma, the message 'You Win' is displayed because the mask is worn correctly.

![image](https://user-images.githubusercontent.com/89971178/131848225-a4ac62c6-fd88-46b2-9979-8faa3a394a2b.png)

If you have any problems with Bubble, I recommend using the **Debugger** function. After setting the 'Slow' mode in the Debugger, you can check the results of each step in the workflow as text and find the bug that needs to be solved.

![image](https://user-images.githubusercontent.com/89971178/131848454-80e15ca2-36a3-4a02-9b64-e858bea17900.png)




