# Exercise 4 - Extend the Dashboard with No Code Features

**Objective:** You should develop a dashboard with No code Features in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** Story designers can leverage a variety of no-code features coming from analytical applications, such as Custom widgets, composite and Custom widget Add-on. 

 **Custom Widgtes:**
 Story designer can now integrate custom widgets into story, to extend the varieties of visualizations and functionalities. With the data binding capability of 
 custom widget, story designer can configure custom widgets like configure a standard SAP Analytics Cloud chart without any coding or scripting knowledge. 

 **Composites:**
 A composite is a combination of widgets with configured data and scripting elements, which can be reused across optimized stories. It can be a unified corporate  
 header or footer, page navigation panel, collapsible section with visualizations, or chart with a button to switch to another chart type or table view. With 
 composites ready to be used in stories, story designers and developers spend less time building stories, and they can do further actions and customizations on the 
 composite as a whole as well, such as changing styling and adding scripts.
 You can create a composite and then import and directly use it in your optimized story as other SAP Analytics Cloud built-in widgets.

**Key Features:**
* Create a composite
* Create a custom widget
* Create a custom widget Add-on
----------------------------------------------------------------------------------------------------------------------------------------

## Level 2 Heading

After completing these steps you will have....

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
