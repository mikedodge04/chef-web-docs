.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

Use the following timers to specify when a notification is triggered:

``:delayed``
   Use to specify that a notification should be queued up, and then executed at the very end of a |chef client| run.

``:immediately``
   Use to specify that a notification should be run immediately, per resource notified.
