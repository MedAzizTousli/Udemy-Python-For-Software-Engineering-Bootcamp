## Question 1
```python
from fastapi.responses import Response

@user_router.patch("/dummy")
async def test_response_code() -> Response:
    return Response(status_code=204)
```
## Question 2
```python
from fastapi import status
from fastapi import Response

@user_router.patch("/dummy")
async def test_response_code() -> Response:
    return Response(status_code=status.HTTP_204_NO_CONTENT)
```
