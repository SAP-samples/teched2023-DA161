# Exercise 5 –  Extend the Dashboard with Scripting

**Objective:** You should develop a basic understanding of scripting capabilities in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** In Exercise 4, our customers were able to extend the dashboard with No code features. while working through this dashboard, they realized that they weren't sure what currency rates were being used for the calculations in the Financial Plan and Employee Plan. We want to provide them a better understanding of what those rates are by utilizing scripting capabilities in SAP Analytics Cloud.

**Key Features:**
* Understand how to add a popup in a dashboard
* Utilize a button to increase user interaction in a popup
* Write scripts to open and close a popup 

⚠️**Disclaimer**
When completing exercises, some data values or screenshots may not match what you see on your screen. 

----------------------------------------------------------------------------------------------------------------------------------------

1. Open the Story **Exercise-5 Extend the Dashbord with scripting** and Click **Edit** 

![image](https://user-images.githubusercontent.com/112718519/198360329-af917931-431d-422c-8b1e-9d3bc1471293.png)

2. Now that we are an editor of the dashboard, we can see that there is a hidden page. Click the **Employee Rates Table** tab.

![image](https://user-images.githubusercontent.com/112718519/198360386-fb87d369-15c7-407b-9627-60410c9ad58d.png)

🚩 The Employee Rates Table provides us with an understanding of the rates that are used for calculations in the Financial Plan and Employee Plan. However, we want to access the Employee Rates Table in an easier way. In order to do that, we want to provide a jumpoff point in the Employee Plan Table that can show us the rates.

3. First, we want to copy the table. Click into the edge of the Table. Right click and click **Copy**. Alternatively, we can also press **CTRL + C**.

![image](https://user-images.githubusercontent.com/112718519/198360455-4d190c51-5297-4694-a9cd-aaf734ac78c8.png)

4. Click on the **Employee Plan** tab

![image](https://user-images.githubusercontent.com/112718519/198360764-e62ddf43-4bf1-4acf-88d4-c0e82c956557.png)

5. Click on the **Left Side Panel** icon 

![image](https://user-images.githubusercontent.com/112718519/198360800-154749b2-b098-47fe-b526-1001ae33651b.png)

6. **Click Outline**

![image](https://user-images.githubusercontent.com/112718519/198360871-38f1af0e-1428-44cd-b977-f6a0fc1c5af1.png)

7. The blue circular dot on the Left Side Panel indicates that Page 3 is the current active page. On Page 3, click on the **More** icon.

![image](https://user-images.githubusercontent.com/112718519/198361779-6e2d33be-311c-4ee2-8131-42d9e6b3f7ee.png)

8. Click **Add Popup** 

![image](https://user-images.githubusercontent.com/112718519/198361559-5daba728-5342-40b4-b2f2-cf0cca8116d5.png)

9. Press **CTRL + V** to paste the Table into the Popup

![image](https://user-images.githubusercontent.com/112718519/198361611-834d1df0-8155-4253-9908-71bbf6f20759.png)

10. Click **Continue**

![image](https://user-images.githubusercontent.com/112718519/198361820-5e046d7c-4c00-46fd-aad7-bfe6884fffc6.png)

⚠️ **Quality check!** Does your Popup look like this?

![image](https://user-images.githubusercontent.com/112718519/198361991-cfea35ae-6888-46b8-a9ab-a60708c09a58.png)

11. We want to resize the Popup in the Styling panel. Click the **Right Side Panel** icon to open the Styling panel. 

![image](https://user-images.githubusercontent.com/112718519/198362025-553f51df-9746-44c5-a092-5d8f5ed1a7d5.png)

12. Once the panel opens, click the top right corner of the panel to switch from the Builder Panel to the Styling Panel

![image](https://user-images.githubusercontent.com/112718519/198371339-148930ed-f28c-4c81-9c27-cb41ef8c032f.png)

13. In the Left Side Panel, click Popup_1 so that we can access the Styling panel for Popup_1 instead of the Table.

![image](https://user-images.githubusercontent.com/112718519/198371355-2f6da041-6aaa-4232-9de6-395aacc144ab.png)

14. In the Styling panel, scroll down until you see the width and height. Change the width to 1700.

![image](https://user-images.githubusercontent.com/112718519/198371385-e35aa5f8-913f-49d1-b031-09f291283f6b.png)

15. Change the height to 524

![image](https://user-images.githubusercontent.com/112718519/198372163-b98fde95-c25f-41aa-ae1e-0856c601048b.png)

16. Click the **Right Side Panel** icon to close the Styling panel

![image](https://user-images.githubusercontent.com/112718519/198371687-a6b2fd8b-9bdf-46ce-a5c2-69ed40dd9292.png)

17. Now, we want to make sure that we have the ability to close the Employee Rates Table in the Popup via a Button. We will add a Button by clicking the **Add** icon in the top panel.

![image](https://user-images.githubusercontent.com/112718519/198372349-d38cfb22-085a-4c1e-bc1b-a87adede9a9a.png)

18. Click **Button**

![image](https://user-images.githubusercontent.com/112718519/198372247-479c7c8b-a15f-443f-9d29-8cf7364d944c.png)

19. We want to move the Button to the top right of the Table. Click the edge of the Button and drag. 

20. Drag the Button to the top right of the Table

![image](https://user-images.githubusercontent.com/112718519/198372490-16749717-1d48-4e71-85a9-35a9fc0d207c.png)

21. We want to rename the Button. Click the **Right Side Panel** icon to open the Styling panel.

![image](https://user-images.githubusercontent.com/112718519/198375040-c2baa745-7e43-429f-837b-74c9e3b2babd.png)

22. Under Text, rename the Button to **Close Rates Table**

![image](https://user-images.githubusercontent.com/112718519/198372847-536e10ab-a61a-403b-960b-221cc7a74652.png)

23. Click the **Right Side Panel** icon to close the Styling panel

![image](https://user-images.githubusercontent.com/112718519/198373024-b10882f9-f8e0-47fb-8bc0-babd9a98449b.png)

24. We want to resize the Button to make it larger. Click on the bottom left corner of the Button.

25. Drag the button to lengthen the width

![image](https://user-images.githubusercontent.com/112718519/198373073-63fac810-13ac-43c4-b114-b0984a126151.png)

26. Now, we will begin the scripting. Click on the **Employee Plan** tab.

![image](https://user-images.githubusercontent.com/112718519/198375091-c5488392-91a1-4d07-905f-2ed040531e2f.png)

27. Click onto the shape. 

![image](https://user-images.githubusercontent.com/112718519/199622168-484e713a-1d1c-4a6c-8aba-f13e77ac25c5.png)

28. In Shape_7, click the **Edit Scripts** icon

![image](https://user-images.githubusercontent.com/112718519/198373227-5aeee0b8-f902-45d7-a291-95d0ef4c684b.png)

29. Click **onClick**

![image](https://user-images.githubusercontent.com/112718519/198373245-3b43abfb-a739-4916-8911-4192dfc3a354.png)

🚩 Welcome to Scripting! Scripting allows you to write scripts that can perform complex actions for widgets, such as customizing user interactions in widgets. While writing the scripts, you can press CTRL + SPACE on your keyboard to show all the available scripting commands. 

30. Type **Popup_1.**

![image](https://user-images.githubusercontent.com/112718519/198373291-5bc09c7d-a9bc-4422-92ed-ce9f3183b880.png)

31. Press **CTRL + SPACE** on your keyboard to open a list of available scripting commands. Click **open**. This command enables the Popup to open when it is clicked.

![image](https://user-images.githubusercontent.com/112718519/198373330-bdd994a8-27ed-47aa-b60c-c1ebf223228e.png)

32. Press the semicolon ; on your keyboard

![image](https://user-images.githubusercontent.com/112718519/198373368-2361e6dc-17ef-4aa3-9294-848b29887099.png)

33. After writing a script to open the Popup, we now want to write another script to close the Popup. Click **Popup_1** in the Left Side Panel.

![image](https://user-images.githubusercontent.com/112718519/198373394-aa91a981-d403-43f4-8ec9-3f084301de64.png)

34. Scroll to the right of the Table until we see the Button. Click on the **Close Rates Table Button**.

![image](https://user-images.githubusercontent.com/112718519/198373419-a2dcb7b4-13f0-4f38-9066-c17616a8d856.png)

35. Click on the **More Actions** icon

![image](https://user-images.githubusercontent.com/112718519/198373468-fe926321-734f-4865-b50d-e9b9180aa4ef.png)

36. In Edit Scripts, click **onClick**

![image](https://user-images.githubusercontent.com/112718519/198373490-c28466c9-ec95-4325-8528-f3c406f2d11b.png)

37. Type **Popup_1.**

![image](https://user-images.githubusercontent.com/112718519/198373522-4ceb9dc2-0c56-4fc2-9c35-9e647b3f2dcd.png)

38. Press **CTRL + SPACE** on our keyboard to show a list of available commands. Click **close**.

![image](https://user-images.githubusercontent.com/112718519/198373590-41bfe86f-18fd-4984-acb6-0fef8688092b.png)

39. Press the semicolon ; on your keyboard

![image](https://user-images.githubusercontent.com/112718519/198373632-d456f5c0-8327-432e-a307-49aa0ddb88a3.png)

40. Now, we will save our dashboard. Under File, click **Save**. Alternatively, you can also press CTRL + S.

![image](https://user-images.githubusercontent.com/112718519/198373645-8907a0a9-9202-4028-8d36-144175a276ee.png)

41. Now, we will go into View mode to test out the Popup. Click **View**, which will bring us to a new tab.

![image](https://user-images.githubusercontent.com/112718519/198373718-bd5d06f8-c61b-46dd-bff6-a628977dd86d.png)

42. Click the Employee Plan tab

![image](https://user-images.githubusercontent.com/112718519/198373764-160d9cc3-3e7d-4717-8e89-627eae9bcb6f.png)

43. Click on the **shape** to launch the Employee Rates Table

![image](https://user-images.githubusercontent.com/112718519/198373797-afbf84fa-7d8b-4dca-8ecb-7a347fbcb9d8.png)

44. Now that the Popup is open, we can now close it. Press on the **Close Rates Table Button**.

![image](https://user-images.githubusercontent.com/112718519/198374002-3e3f00f7-78be-44fa-b2ed-3fe6eca61c15.png)


## Summary

**You have completed the entire Integrating Scripting section!**

**You are now able to:**
* Understand how to add a popup in a dashboard
