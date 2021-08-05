# Bagisto Changes

These are the changes from the version 1.3.1 to 1.3.2,

## Changes from the web vital

- For the velocity theme, the `velocity.js` file is divided into two files i.e. `velocity-core.js` and the `velocity.js` file. In `velocity-core.js`, all core dependencies like jQuery, bootstrap js, Vue js are added and in `velocity.js` all the components are present which is bootstrapped by the `velocity-core.js`.

- All these components are minified now, `quantity-changer`, `mini-cart`, `slider-component`, and `searchbar-component`.

- These components are added `hot-categories`, `popular-categories`, `sidebar-header`, `right-side-header` and `mobile-header`.

- This folder  i.e. `packages/Webkul/Velocity/src/Resources/views/shop/UI` is completely removed. The files inside this folder contain the components which are already minified so not needed. Make sure if you included these files in your modules, use the direct component rather than including the file.

- In this folder i.e. `packages/Webkul/Velocity/src/Resources/views/shop/layouts/particals` three files (`compare.blade.php`, `wishlist.blade.php` and `search-bar.blade.php`) are given. All these files are having individual components. For `compare.blade.php` and `wislist.blade.php`, you can use the `isText` prop to disable the text for mobile.

- If still needs to check more changes then feel free to check this [link](https://github.com/bagisto/bagisto/pull/5020/files).
