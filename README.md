# forms-demo

You're welcome to check the commit history in this repository to see what changes were made.

On a high level, this is what was done to display the form:

1) Create a TaskForm class in todoapp/forms.py which is associated with the Task model
2) In my view for index.html, create a new empty instance of TaskForm and pass it to the template
3) In the template, render the form by creating a `<form>` element, putting `{{ form.as_p }}` inside of the `<form>` element instead of manually specifying labels and inputs for the form.

This is what was done to process submitted forms:

1) Create a new view that is responsible for handling submitted forms (e.g. `create_task`).
2) Create a new instance of  `TaskForm` and pass `request.POST` to the constructor.
3) Check if the form is valid
4) Call `form.save()` to save the new `Task` to the database
5) Redirect to the homepage
