About
=====

This script protects a form from being navigated away from by throwing up a confirmation dialog if information has been entered but not saved.

Requirements
------------

* jQuery

Installation
------------

    <script src="form-protector.js"></script>

Example
-------

To protect a form with id `MyFormId`:

    <script>
        $(document).ready(function () {
            formProtector.protect('MyFormId');
        });
    </script>

This will produce a confirmation dialog if any `<input>`, `<select>`, or `<textarea>` has its value changed and the user navigates away by any means other than submitting the form.

If you want to manually mark a form as having been changed:

    <script>
        $(document).ready(function () {
            formProtector.setChanged('MyFormId');
        });
    </script>

If you want to manually mark a form as having been saved (e.g. if you have an asynchronous function that stores form data):

    <script>
        $(document).ready(function () {
            formProtector.setSaved('MyFormId');
        });
    </script>