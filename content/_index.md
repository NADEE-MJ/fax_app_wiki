---
title: About
type: docs
---

# About

{{< columns >}}

## What is fax app?

placeholder **placeholder** _placeholder_

<--->

## Setup

placeholder **placeholder** _placeholder_

{{< /columns >}}


## Example

placeholder **placeholder** _placeholder_

~~~python
@router.put("/me", response_model=schemas.User)
def update_user_me(
    *,
    db: Any = Depends(deps.get_db),
    user_update: schemas.UserUpdate,
    current_user: UserProfile = Depends(deps.get_current_active_user),
) -> Any:
    """
    Update own user.
    """
    user = crud.user.update(db, db_obj=current_user, obj_in=user_update)
    return user
~~~

## Created With

placeholder **placeholder** _placeholder_
