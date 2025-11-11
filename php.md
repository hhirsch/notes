# PHP
I really enjoyed *Front Line PHP* by Brent Roose and Freek Van der Herten.
The book gave a nice overview of the newest PHP features and some opinions about design and patterns.

## No discard attribute
```php
#[\NoDiscard]
function getImportantErrorString(): string {
    produceSideEffect();
    return "There was an error";
}
```
You should either cast to void or handle the return value. Otherwise a PHP warning will be triggered.

Cast to void like this:
```php
(void)getImportantErrorString();
```
