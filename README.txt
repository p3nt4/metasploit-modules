This module "carves" a hash in the registries to set it as a user password.

The benefits are:
1/ It doesn't change the "password last changed" field
2/ You can set a hash directly, so you can change a user's password and revert it without cracking it's hash.

I have tested it in Windows 7 and 8.1 successfully.
Does not seem to work on 10, not sure why.

Usage:
run post/windows/manage/hashcarve user=test pass=password
run post/windows/manage/hashcarve user=test pass=nthash
run post/windows/manage/hashcarve user=test pass=lmhash:nthash

This work is based on the hashdump implementation.
