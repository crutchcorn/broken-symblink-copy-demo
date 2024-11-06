# Broken Symlink Vite Build Demo

This is a demo project to show how Vite build breaks when there is a broken symlink in the project.

## Steps to reproduce

1. Clone this repository
2. Run `npm install`
3. Run `npm run build`
4. See the error

This happens because the `copyDir` utility in Vite does not handle broken symlinks properly when inside of `public`. It tries to copy the broken symlink and fails.
