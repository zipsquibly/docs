<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
import os
from syllable_sdk import Syllable

s = Syllable(
    api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
)

res = s.agents.list()

if res is not None:
    # handle response
    pass
```

</br>

The same SDK client can also be used to make asychronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
import os
from syllable_sdk import Syllable

async def main():
    s = Syllable(
        api_key_header=os.getenv("SYLLABLE_API_KEY_HEADER", ""),
    )
    res = await s.agents.list_async()
    if res is not None:
        # handle response
        pass

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->