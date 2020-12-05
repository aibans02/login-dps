# login-dps
## Exercise 1 - Armando Ibán
### https://github.com/aibans02/login-dps 

----------------------------------------------------------------------

### Issues

In LoginServlet.java the next issues were founded:

  1. **IDS00-J. Prevent SQL injection. In Line 21.** Password is compared directly with a value. No previus check
  2. **IDS01-J. Normalize strings before validating them. Line 21.** Password is validated before normalize
  3. **IDS03-J. Do not log unsanitized user input. Line 25.** Cookie is added with name before sanitize
  4. **IDS10-J. Don’t form strings containing partial characters. Lines 18-19.** Both name and password are saved as string without check
  5. **IDS14-J. Do not trust the contents of hidden form fields. Line 21.** Password field is hidden and is compared without checking
  6. **SEC02-J. Do not base security checks on untrusted sources. Line 21.** Password check is performed with the data input from user that is not validated
  7. **MSC03-J. Never hard code sensitive information. Line 21.** Correct password is harcoded

In ProfileServlet.java the next issues were founded:

  1. **IDS00-J. Prevent SQL injection. In Line 20.** Name is got from cookie, which is not verified
  2. **IDS01-J. Normalize strings before validating them. Line 21.** Name is validated before check
  3. **IDS10-J. Don’t form strings containing partial characters. Lines 20.** Name is saved as string without check
  4. **SEC02-J. Do not base security checks on untrusted sources. Line 21.** Name is taken from cookie and it is not validated previusly
  5. **MSC03-J. Never hard code sensitive information. Line 21.** Incorrect name is harcoded
  6. **MSC11-J. Do not let session information leak within a servlet. Line 23** Name is printed
  
### Environment

  Apache Tomcat 9
  
  Eclipse IDE
  
  openjdk 11.0.9
