# **Mail**
## Project 3 - CS50W Submission

### **Send Mail**
Users can click on the `compose` button to switch the page view to an email compose form. On the submission of the form, it's made a `POST` request to the API. 

If there's some error in the response, a dismissible alert will show up. Otherwise the email will be sent and the user will be taken to the `sent` mailbox. 

### **Mailbox**
Using the buttons on the top of the main page users can switch between their mailboxes (`inbox`, `sent` and `archived`). On the click of one of these buttons, a `GET` request is made to the API, receiving back the emails for the mailbox selected.

When the results get received, the user will see each of the emails of the selected mailbox in a "box", displaying the `sender`, `subject` and `timestamp` of the email. If the email has been read, the box will have a gray background, otherwise it will be white.

### **View Email**
If any of the emails are clicked, the view will switch to a full view of the emai. The page will display the `sender`, `recipients`, `subject`, `timestamp`, and `body`.

When the user click on the email, it will be marked as read, and for now on will have a gray background.

### **Archive and Unarchive**
On the full email view, there's a button with either the text "Archive" or "Unarchive" depending on the value of `archive` in the email. 

If the user clicks on this button, it will change the value of `archive` to the opposite of it's previous value.

### **Reply**
On the full email view, there's a button with text "reply". When clickes, the view will switch to the compose form.

In the compose form somethings will be already filled.
* The `recipient` is set as the `sender` of the original email.
* The original subject is kept, adding a "Re: " to wathever it was.
    * If the subject already had a "Re: " before, it won't be repeated.
* The reply's body will be pre-filled as "On `original timestamp` `original sender` wrote: `original body`"

### **External Links**
**Video Demonstration**: https://www.youtube.com/

**Try the project here**: https://mail-project3-cs50w.herokuapp.com/