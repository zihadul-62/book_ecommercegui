# E-Commerce Book  Python GUI Edition

This version is based on the uploaded original `ecommerce.db` and the C project's SQLite schema.

## Run
- Keep `main.py` and `ecommerce.db` in the same folder.
- Run `python main.py` from a terminal or VS Code.
- Python's `tkinter` and `sqlite3` are standard-library modules in most Python installations.

## Features
- User registration/login and password reset by username + registered email
- Admin login
- Book catalogue search
- Shopping cart, multi-item checkout and tiered discount (20% at >= Tk 1999, 10% at >= Tk 1499, 5% at >= Tk 999)
- Delivery address and phone collection
- Stock decrement on checkout
- User order history
- Admin book add/edit/delete
- Admin order status update

## Important
1. Back up `ecommerce.db` before testing. The included database is the user's uploaded database and may contain real project data.
2. The uploaded database stores passwords as plain text, matching the original C schema. This version preserves that schema for compatibility; for a real deployed app, migrate to salted password hashes and avoid revealing passwords.
3. The C code applies a discount to each cart line and creates one order row per cart item; this version follows that behavior.
4. Your `user.c` / `total.h` files were not included in this upload set, so this GUI reconstructs the customer-facing navigation from the provided modules and README rather than claiming byte-for-byte behavior equivalence.
5. `setup.sql` is included for reference only. Do not rerun it over your existing database unless you intentionally want to recreate/seed a database; keep backups.
