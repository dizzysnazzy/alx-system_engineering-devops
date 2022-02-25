# Postmortem

![post mortem](post-mortem.png)

## Issue Summary

I finished a hotel management system project on Java and shared it to an interested user for implimentation. Since she was my first client i told her not to only fully rely on the system but also keep the data manually as she used before as we monitor if the system has some bugs. Everything went fine on the first day, but on the second day, i received a call from the client saying that the 'Data is saved' pop-up did not appear after clicking 'Save' button, this means that the food ordered could not be saved to the database. The issue started on the second day when she tried to take the first order from the customer. The client did not fill one of the text-field and thus could not save the order with one empty text-field.

## Timeline

+ 09:00 am EAT - Received a call from my client immediately when she could not get the 'Data saved' pop-up
+ 09:20 am EAT - I investigated the database attributes and compared to the ones in the system.
+ 10:15 am EAT - Realized that the date had not been set on the JDateChooser field to show the current date.
+ 10:22 am EAT - The user had to update the time everyday she logs-in to the system thats why the issue came up on the second day.
+ 10:50 am EAT - I updated the JDateChooser to autoupdate the date and time and made it uneditable to the user.

## Root Cause And Resolution

The user did not fill in the current date in the date field and therefore the 'SAVE' button could not be able to save the data since there was a missing value in the date attribute.
I updated my code by making the JDateChooser to autoupdate the date and time and made it uneditable to the user to avoid any further errors. So the user didn't have to worry about the update everyday she logs-in.

## Corrective And Preventative Measures

+ The date and time must be automated all the time so that the user won't be filling it.
+ Make sure the JDateChooser jar file is added to the palette.
