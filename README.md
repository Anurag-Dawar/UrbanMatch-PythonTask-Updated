# UrbanMatch-PythonTask-Updated

## Brief Report

### Approach

1. **Add User Update Endpoint:**
   - Implemented an endpoint to update user details by ID.
   - Used `PUT` method to handle the update request.
   - Validated if the user exists and then updated the user details in the database.

2. **Add User Deletion Endpoint:**
   - Implemented an endpoint to delete a user profile by ID.
   - Used `DELETE` method to handle the deletion request.
   - Validated if the user exists and then deleted the user from the database.

3. **Find Matches for a User:**
   - Implemented an endpoint to find potential matches for a user based on their profile information.
   - Used `GET` method to handle the request.
   - The matching logic considers the user's gender, city, and interests to find potential matches.

4. **Add Email Validation:**
   - Added validation to ensure the email field in user profiles contains valid email addresses.
   - Used `EmailStr` from Pydantic to enforce email validation.

### Assumptions

1. **User Interests:**
   - Assumed that user interests are stored as a list of strings.
   - Used SQLAlchemy's array type for storing interests.

2. **Email Validation:**
   - Assumed that email addresses should be validated strictly according to standard email format.

3. **Matching Criteria:**
   - Assumed that a potential match is based on the opposite gender, same city, and overlapping interests.
   - Used simple SQL filtering for matching criteria.

4. **Endpoints:**
   - Followed RESTful principles for naming and structuring the endpoints.

### Files Modified

- `main.py`: Added update, delete, and match endpoints.
- `schemas.py`: Added email validation.

### Endpoints Added

1. **Update User Endpoint**

```PUT /users/{user_id}```

Update user details by ID.

2. **Delete User Endpoint**

```DELETE /users/{user_id}```

Delete user profile by ID.

3. **Find Matches Endpoint**

```GET /users/{user_id}/matches```

Find potential matches for a user based on profile information.

