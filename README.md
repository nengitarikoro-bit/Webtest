The W3C Markup Validation Service was used to thoroughly test this project as it was being developed. The main technical problems found and the fixes put in place are listed below:

Resolution of File Paths (Relative vs. Absolute)The problem: Local drive paths, such as `C:\Users\...`, were identified by the validator as containing prohibited characters. As a fix, all file references were changed to Relative Paths (`Images/logo.jpg`). This guarantees that the website will continue to be functional and portable across various hosting environments.

2. Using Tag Nesting and Semantic Hierarchy The problem: "Heading cannot be a child of another heading" along with "Element p not allowed as child of h3."
3. 
The HTML structure was restructured to adhere to an appropriate parent-child hierarchy. Now, text is contained in `<p>` or `<div>` tags, and headings are only used for titles. 3. Attributes & Image Optimisation Issue: The validator disallowed percentage values inside HTML `width` properties, such as `37.5%`. All responsive styling has been moved to the CSS `style.css`.

Correcting Syntax
Fatal parsing problems were triggered by unclosed elements (`<header>`) and stray end tags (`</div>`).
In order to make sure that each opening tag has a matching ending tag in the proper order (First-In-Last-Out), a thorough audit of the DOM tree was conducted.
