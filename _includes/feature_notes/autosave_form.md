The "Autosave Form" module provides an autosave feature for all forms. The autosave submits will be triggered every 60 seconds and store the changes from the currently logged-in user in the database.

In Thunder, it is active for node articles and basic pages and all media types.

## Steps to present the module

For demonstration purpose, it's recommended to decrease the interval to trigger the autosave on admin/config/content/autosave_form.

Autosaves only works on existing entities, for now, so navigate to one.
For example, you can use Node 6 from the Thunder Demo module.

 * Wait for the first "Saving draft..." without doing any changes
 * Reload the page and you will notice no restore messages.
 * Now change the title to "My new title."
 * Reload the page again and you will get a restoring message.
 * Resume editing
 * Add a new tag "CMS"
 * Add a new image paragraph between some existing paragraphs.
 * Wait for the first "Saving draft..." and reload the page again
 * Resume editing and verify that your changes are still there
 * Reload again and discard the changes
 * Your initial article is back
