---
title: Listening for events
weight: 7
---

The package fires events where you can listen for to perform some extra logic.

## `\Spatie\Multitenancy\Events\MakingTenantCurrentEvent`

This event will fire when a tenant is being made the current one. At this point none of [the tasks](/docs/laravel-multitenancy/v4/using-tasks-to-prepare-the-environment/overview/) have been executed.

It has one public property `$tenant`, that contains an instance of `Spatie\Multitenancy\Models\Tenant`.

## `\Spatie\Multitenancy\Events\MadeTenantCurrentEvent`

This event will fire when a tenant has been made the current one. At this point the `makeCurrent` method of all of [the tasks](/docs/laravel-multitenancy/v4/using-tasks-to-prepare-the-environment/overview/) have been executed. The current tenant also have been bound as `currentTenant` in the container.

It has one public property `$tenant`, that contains an instance of `Spatie\Multitenancy\Models\Tenant`.

## `\Spatie\Multitenancy\Events\ForgettingCurrentTenantEvent`

This event will fire when a tenant is being forgotten. At this point none of [the tasks](/docs/laravel-multitenancy/v4/using-tasks-to-prepare-the-environment/overview/) have been executed.

It has one public property `$tenant`, that contains an instance of `Spatie\Multitenancy\Models\Tenant`.

## `\Spatie\Multitenancy\Events\ForgotCurrentTenantEvent`

This event will fire when a tenant has been forgotten. At this point the `forgotCurrent` method of all of [the tasks](/docs/laravel-multitenancy/v4/using-tasks-to-prepare-the-environment/overview/) have been executed. `currentTenant` in the container has been emptied.

## `\Spatie\Multitenancy\Events\TenantNotFoundForRequestEvent`

This event will fire when no tenant was found by the `findForRequest()` method of the `TenantFinder` for the given request.

It has one public property `$request`, that contains an instance of `Illuminate\Http\Request`.
