## Question 1
```python
def update_user_only(full_user_profile: UserProfileInfo, user_id: int) -> FullUserProfile:
    global profile_infos
    global users_content

    short_description = full_user_profile.short_description
    long_bio = full_user_profile.long_bio

    profile_infos[user_id] = {
        "short_description": short_description,
        "long_bio": long_bio
    }

    user_content = users_content[user_id]
    profile_info = profile_infos[user_id]

    user = User(**user_content)

    full_user_profile = {
        **profile_info,
        **user.dict()
    }

    return FullUserProfile(**full_user_profile)

@app.patch('/user/{user_id}', response_model=FullUserProfile)
def update_only(user_id: int, full_user_profile: UserProfileInfo):
    new_full_user_profile = update_user_only(full_user_profile, user_id)
    return new_full_user_profile
```