# Conditionals
## Encapsulate Conditionals
```php
// Inline conditional (harder to read)
if ($user->isActive && $user->subscription->isValid() && !$user->isBanned()) {
    $this->grantAccess($user);
}

// Encapsulated conditional (better readability)
if ($user->canAccessPlatform()) {
    $this->grantAccess($user);
}
```
This makes code more:
- Readable – intent is clearer (e.g., if ($user->isEligibleForDiscount()) is easier to read than raw logic inline).
- Reusable – encapsulated logic can be reused in multiple places.
- Maintainable – if the business rule changes, you update one place, not scattered if statements.

**Rule of Thumb**
- Small, obvious conditionals -> keep inline.
- Complex, business-rule conditionals -> encapsulate for clarity and maintainability.
