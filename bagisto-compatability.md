# Bagisto Changes

These are the changes from the version 1.3.1 to 1.3.2,

## Changes from the web vital (Medium Severity)

- For the velocity theme, the `velocity.js` file is divided into two files i.e. `velocity-core.js` and the `velocity.js` file. In `velocity-core.js`, all core dependencies like jQuery, bootstrap js, Vue js are added and in `velocity.js` all the components are present which is bootstrapped by the `velocity-core.js`.

- All these components are minified now, `quantity-changer`, `mini-cart`, `slider-component`, and `searchbar-component`.

- These components are added `hot-categories`, `popular-categories`, `sidebar-header`, `right-side-header` and `mobile-header`.

- This folder  i.e. `packages/Webkul/Velocity/src/Resources/views/shop/UI` is completely removed. The files inside this folder contain the components which are already minified so not needed. Make sure if you included these files in your modules, use the direct component rather than including the file.

- In this folder i.e. `packages/Webkul/Velocity/src/Resources/views/shop/layouts/particals` three files (`compare.blade.php`, `wishlist.blade.php` and `search-bar.blade.php`) are given. All these files are having individual components. For `compare.blade.php` and `wislist.blade.php`, you can use the `isText` prop to disable the text for mobile.

- If still needs to check more changes then feel free to check this [link](https://github.com/bagisto/bagisto/pull/5020/files).

- Refernece PR: [#5020](https://github.com/bagisto/bagisto/pull/5020)

## Changes from security fixes (High Severity)

- These routes i.e. `address.delete`, `customer.orders.cancel`, `customer.review.delete` and `customer.review.deleteall` methods are changed from `GET` to `DELETE` and `POST` respectively. `GET` is only use for retrieving data.

- Maybe if you forgot to change then surely this will impact your project. Make sure it should be updated.

- Refernece PR: [#4996](https://github.com/bagisto/bagisto/pull/4996) and [#4998](https://github.com/bagisto/bagisto/pull/4998)

## Downloadable product medias are moved to private disk (Medium Severity)

- If someone wants to integrate into the existing project and the downloadable links are broken, then move your downloadable links folder to a private disk, and the broken link got fixed.

- Refernece PR: [#4966](https://github.com/bagisto/bagisto/pull/4966)

## Changes from invoice prefixes (Medium Severity)

- Moved sequencer class from shop package to sales package, as orders and invoices are part of the sales. This will not impact as there is only one key and that one is in the repository.

- Enhanced and scaled the `Sequencer` class.

- As per the existing project perspective, `increment_id` by default is going null, so for displaying portion it will first check `increment_id` if not found then it will give the actual `id`.

- In the core config, moved all the invoice settings to the new tab name `Invoice Settings` so make sure reset the value for the `Invoice Slip Design`.

- Refernece PR: [#4956](https://github.com/bagisto/bagisto/pull/4956)

## Changes from `.env` (Low Severity)

- Just capitalized the  `fixer_api_key` in `.env` to have consistency and `.env` standard.

- If you have this key in your `.env` and you are using this just make sure you capitalize your key also.
