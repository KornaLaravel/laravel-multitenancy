<div align="left">
    <a href="https://spatie.be/open-source?utm_source=github&utm_medium=banner&utm_campaign=laravel-multitenancy">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://spatie.be/packages/header/laravel-multitenancy/html/dark.webp?1">
        <img alt="Logo for laravel-multitenancy" src="https://spatie.be/packages/header/laravel-multitenancy/html/light.webp?1">
      </picture>
    </a>

<h1>Unopinionated multitenancy package for Laravel</h1>

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/laravel-multitenancy.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-multitenancy)
[![GitHub Tests Action Status](https://img.shields.io/github/actions/workflow/status/spatie/laravel-multitenancy/run-tests.yml?branch=main&label=Tests&style=flat-square)](https://github.com/spatie/laravel-multitenancy/actions?query=workflow%3Arun-tests+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/spatie/laravel-multitenancy.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-multitenancy)
    
</div>

This package can make a Laravel app tenant aware. The philosophy of this package is that it should only provide the bare essentials to enable multitenancy.

The package can determine which tenant should be the current tenant for the request. It also allows you to define what should happen when switching the current tenant to another one. It works for multitenancy projects that need to use one or multiple databases.

Before starting with the package, we highly recommend first watching [this talk by Tom Schlick on multitenancy strategies](https://tomschlick.com/laracon-2017-multi-tenancy-talk/).

The package contains a lot of niceties such as making queued jobs tenant aware, making an artisan command run for each tenant, an easy way to set a connection on a model, and much more.

Are you a visual learner? Then watch [this video](https://spatie.be/videos/laravel-package-training/laravel-multitenancy) that covers how you can use laravel-multitenancy and how it works under the hood.

## Support us

[<img src="https://github-ads.s3.eu-central-1.amazonaws.com/laravel-multitenancy.jpg?t=1" width="419px" />](https://spatie.be/github-ad-click/laravel-multitenancy)

We invest a lot of resources into creating [best in class open source packages](https://spatie.be/open-source). You can support us by [buying one of our paid products](https://spatie.be/open-source/support-us).

We highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address on [our contact page](https://spatie.be/about-us). We publish all received postcards on [our virtual postcard wall](https://spatie.be/open-source/postcards).

## Documentation

You can find the entire documentation for this package [on our documentation site](https://docs.spatie.be/laravel-multitenancy).

## Testing

You'll need to create the following 3 local MySql databases to be able to run the test suite:

- `laravel_mt_landlord`
- `laravel_mt_tenant_1` 
- `laravel_mt_tenant_2`

You can run the package's tests:

``` bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](https://github.com/spatie/.github/blob/main/CONTRIBUTING.md) for details.

## Security

If you've found a bug regarding security please mail [security@spatie.be](mailto:security@spatie.be) instead of using the issue tracker.

## Credits

The code of this package is based on the code shown in [the Multitenancy in Laravel series](https://www.youtube.com/watch?v=592EgykFOz4)  by Mohamed Said

- [Freek Van der Herten](https://github.com/freekmurze)
- [All Contributors](../../contributors)

## Alternatives

- [tenancy/tenancy](https://tenancy.dev)
- [stancl/tenancy](https://tenancyforlaravel.com)
- [gecche/laravel-multidomain](https://github.com/gecche/laravel-multidomain)
- [romegadigital/multitenancy](https://github.com/romegasoftware/multitenancy)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
