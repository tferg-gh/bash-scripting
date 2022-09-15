# Return Status

## Success

	Command should return a status of **0**.

## Failure

	Command should return a **non-zero** status.

> Return values can range from **0** to **255**. They can not be negative.

> The return value of the last command executed is captured in the special character **$?**.

> Many programs signal different types of failure with different return values.
