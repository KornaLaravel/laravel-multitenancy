---
title: Working with the current tenant
weight: 3
---

There are several methods available to get, set and clear the current tenant. All methods are available using the Tenant model directly, or through the Laravel Service Container `app(IsTenant::class)`.

### Finding the current tenant

You can find the current tenant like this:

```php
// Model
Tenant::current(); // returns the current tenant, or if no tenant is current, `null`

// Service Container
app(IsTenant::class)::current(); // returns the current tenant, or if no tenant is current, `null`
```

A current tenant will also be bound in the container using the `currentTenant` key.

```php
app('currentTenant'); // returns the current tenant, or if no tenant is current, `null`
```

### Checking if there is a current tenant

You can check if there is tenant set as the current one:

```php
// Model
Tenant::checkCurrent(); // returns `true` or `false`

// Service Container
app(IsTenant::class)::checkCurrent(); // returns `true` or `false`
```

### Manually setting the current tenant

You can manually make a tenant the current one by calling `makeCurrent()` on it.

```php
$tenant->makeCurrent();
```

When a tenant is made the current one, the package will run the `makeCurrent` method of [all tasks configured](/docs/laravel-multitenancy/v4/using-tasks-to-prepare-the-environment/overview/) in the `switch_tenant_tasks` key of the `multitenancy` config file.

### Forgetting the current tenant

You can forget the current tenant:

```php
// Model
Tenant::forgetCurrent();
Tenant::current() // return null;

// Service Container
app(IsTenant::class)::forgetCurrent();
app(IsTenant::class)::current(); // return null
```

If there was no tenant current when calling `forgetCurrent`, the function will do nothing.
