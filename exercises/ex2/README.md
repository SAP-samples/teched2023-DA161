# Exercise 2 - Expand the Dashboard with Core Add-ons





## Exercise 2.1 View Time Toolbar Customization


Objective: You should develop a basic understanding on how to create Customize your toolbar for various experiences of SAP Analytics Cloud Stories.

Estimated Time: 15 mins

Exercise Description: You as a Dashabord designer want to control the toolbar experience for your end users, and having all the toolbar features is not really required for end users.

Key Features:

Define what view mode of the story you need to control for your end users view vs embed mode of your stories.
Learn you to control the toolbar features via story settings.




## Exercise 2.2 Create a Variance within a Story

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)

## Exercise 2.3 Create a threshold
