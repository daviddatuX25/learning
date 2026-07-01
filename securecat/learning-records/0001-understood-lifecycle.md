# Learning Record 0001: Understood the Laravel Request-Response Lifecycle

**Date:** 2026-07-01
**Lesson:** 0001-request-lifecycle.html

## What I learned

- A request passes through a 9-stage pipeline: entry (index.php) -> kernel -> middleware stack -> router -> policy -> controller -> shared props -> Inertia render -> Svelte component
- Middleware is a stack (onion pattern) — each layer can short-circuit or pass through
- The `role` middleware (EnsureUserHasRole) is a 29-line class that checks user roles and aborts with 403 if unauthorized
- Policies add a second layer of authorization beyond route middleware
- Eloquent's `->with()` eager-loading prevents N+1 query problems
- Inertia bridges Laravel and Svelte by sending JSON with a component name, avoiding full page reloads on subsequent visits
- Shared props in HandleInertiaRequests are available on every page via `$page.props`

## Key insight

The controller should be thin — gather data, pass to Inertia. Complex logic belongs in service classes. ExamSessionController is 1,012 lines, which is a sign it should be refactored.

## Questions for next session

- How do Form Requests work separately from controllers?
- What's the difference between middleware and policy authorization?
- Why does SecureCAT have 0 tests? What would testing look like?

## Resources consulted

- SecureCAT `routes/web.php`
- `app/Http/Controllers/Admin/ExamSessionController.php` (index method)
- `app/Http/Middleware/EnsureUserHasRole.php`
- `app/Http/Middleware/HandleInertiaRequests.php`
- `app/Providers/AppServiceProvider.php`
- `resources/js/Layouts/AuthenticatedLayout.svelte`
