# user/del.php
Edition:
zzcms8.3
user/del.php


# 0x01  Vulnerability 

![enter description here](./images/1530536565883.png)


There is unlink($f) to delete any file by controlling the value of $f


# 0x02 Control $f

This variable is obtained by querying the img path in the zzcms_main data table.
So first write the relative path to the file to be deleted in the zzcms_main table.

# 0x03 Insert data into zzcms_main
Code positions to user/zssave.php

![enter description here](./images/1530536846869.png)


Payload is as follows, directly post action=add&img=/user/index.php

![enter description here](./images/1530536866000.png)

# 0x04 Delete Files


This requires a burst of id (id value can be blown)

![enter description here](./images/1530536892262.png)

![enter description here](./images/1530537000778.png)


delete  user/index.php successfully
