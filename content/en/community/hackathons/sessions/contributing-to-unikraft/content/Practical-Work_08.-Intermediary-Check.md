Until now we have registered the library and its sources, and we should be able to compile an unikernel with it *if it doesn't have any more unresolved dependencies*.
Move the `work/02-task-porting/src/apps/app-kdtree` application in the `$UK_APPS` directory, fill its `Makefile`, and use it to build an unikernel with our ported library as a dependency!

If needed, provide additional flags in order to suppress the compile warnings generated by this library.

**Note**: You can leave the application's `main() function empty, the resulted unikernel will just print the `Unikraft` banner.

**Hint**: You can readme, but the solution isn't here.
