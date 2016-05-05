The twelve-factor app
=====================

I. Codebase
-----------
*One codebase tracked in revision control, many deploys*

II. Dependencies
----------------
*Explicitly declare and isolate dependencies*

III. Config
-----------
*Store config in the environment*

> The app stores config in environment variables that are easy to change between
> deploys without changing any code. They are never grouped together as
> "environments" (does not scale), but instead are independently managed
> for each deploy.

IV. Backing Services
--------------------
*Treat backing services as attached resources*

> The code for an app makes no distinction between local and third party services.

V. Build, release, run
----------------------
*Strictly separate build and run stages*

VI. Processes
-------------
*Execute the app as one or more stateless processes*

> Processes are stateless and share-nothing. Any data that needs to persist must
> be stored in a stateful backing service, typically a database.
> Sticky sessions are a violation and should never be used or relied upon.

VII. Port binding
-----------------
*Export services via port binding*

VIII. Concurrency
-----------------
*Scale out via the process model*

IX. Disposability
-----------------
*Maximize robustness with fast startup and graceful shutdown*

X. Dev/prod parity
------------------
*Keep development, staging, and production as similar as possible*

> Make the following gap as small as possible:
> - The time gap: Time between writing code and deploy of it.
> - The personell gap: Developers write code, ops deploy it.
> - The tools gap: Development and production tools.

XI. Logs
--------
*Treat logs as events streams*

> The app never concerns itself with routing or storage of its output.

XII. Admin processes
--------------------
*Run admin/management tasks as one-off processes*

