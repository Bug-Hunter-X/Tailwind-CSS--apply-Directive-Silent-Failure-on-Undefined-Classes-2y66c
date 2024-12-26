# Tailwind CSS @apply Directive Silent Failure on Undefined Classes

This repository demonstrates a subtle bug in Tailwind CSS involving the `@apply` directive. When `@apply` is used with a class that is not defined, there is no error thrown. This can lead to difficult-to-debug styling issues because the missing class won't be obvious. 

## Bug Description

The `@apply` directive silently ignores undefined classes.  This means that if you make a typo in a class name or reference a class that isn't included in your `tailwind.config.js` file, the application will continue without throwing any errors. The unintended result is that the expected styling will not be applied, making it hard to identify the cause of styling errors.