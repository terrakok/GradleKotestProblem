Call `./gradlew tasks` to see the issue with the configuration

Comment the `kotest` plugin in the root build script to fix it

The root case is: if project has applied plugins: KGP 1.9.20 and kotest 5.7.2 (which depends on older KGP) then the build script compilation will fail because there will be the old KGP in compile classpath.
