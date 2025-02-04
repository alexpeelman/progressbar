# Changelog

 * `0.8.0`:
     - Supports loggers (PR #54) by factoring out progress bar consumers and renderers. This allows progress bars to be used with logging libraries such as SLF4J. This PR fixes #12 and #18. Thanks @alexpeelman !
     - Dependency version bump.

 * `0.7.4`:
     - Fixes the bug of slow exit with fast jobs (#50, PR #51). Thanks @meawoppl @denisrosset !
     - Dependency version bump.
 
 * `0.7.3`:
     - Added support for customizing the decimal format of speed display (PR #49). Thanks @wfxr !
     
 * `0.7.2`:
     - Added support for wrapping around `Spliterator`s and `Stream`s. Streams could be either sequential or parallel (#44). Thanks @michaelmior !
     - Added support for displaying speed with unit (PR #43). Thanks @dani909 !

 * `0.7.1`:
     - Fixed the problem of not properly closing the JLine `Terminal` object (#40). Thanks @voseldop !
     - Suppressed JLine warning if a dumb terminal is created (partially fixed #42). Thanks @BuZZ-DEE !
     - Documentation: 
         - Moved `CHANGELOG.md` to the home directory and created a symlink in the `docs/` folder to it (PR #41). Thanks @koppor !
         - Fixed bug (demo code was wrong) in the declarative usage section (PR #39). Thanks @AbhinavVishak !

 * `0.7.0`:
     - Utilized the try-with-resource pattern for the Java imperative syntax, deprecating `ProgressBar#start` and `ProgressBar#stop`.
     - Introduced units for progress bar that enables showing the total amount of work in some unit (e.g. MB / GB) (#33).
     - Introduced the builder pattern for constructing progress bars (instead of lots of different constructors).
     - Added declarative usage that wraps around `InputStream`, which enables tracking the progress of reading a large file or stream (#34).
     - Progress bars are now colorful by default using ANSI color codes.
     - Documentation:
        - Brand new `mkdocs` Material-style documentation! 
 
 * `0.6.0`: 
 
     - Added declarative usage that wraps around `Iterator` and `Iterable`.
     - Updated `jline` dependency to JLine 3. 
     - Fixed problem in IntelliJ console. Thanks @saidaspen, @albancolley, @felixdivo, @AbhinavVishak !
     - Fixed warning about encoding during Maven build. Thanks @khmarbaise !
     - Fixed Java version in Maven build. Thanks @ccamel !
 
 - `0.5.5`: Fixed the problem of the progress bar being stuck if it finishes too fast. 
 Fixed the problem of `StringIndexOutOfBoundsException` error when the console width is too small. 
 Thanks @bwittwer, @rholdberh and @bubyakin !
 - `0.5.4`: Added indefinite progress bar support.
 - `0.5.3`: Type of max/current of a progress bar is changed from `int` to `long`. Thanks @vitobellini ! 
 - `0.5.2`: Methods now returns `this`. This simplifies the initialization: Now you can do `pb = new ProgressBar(...).start()`. Extra messages
 that are too long are trimmed properly. Thanks @mattcg !
 - `0.5.1`: Fixed the refresh problem when progress ended. Added style (Unicode block characters / pure ASCII) support.
 - `0.5.0`: Separated the progress bar thread from the main thread for better performance. Fixed the character offset issue. Thanks @rualpe !
 - `0.4.3`: Changed the symbols to box-drawing characters; more fine-grained display. Thanks @hrj !
 - `0.4.2`: Default output stream is changed to `System.err`; can be customized in constructor. Thanks @AluisioASG !
 - `0.4.1`: Added a `stepTo` method to `ProgressBar`s. Thanks @svenmauer !
 - `0.4.0`: Migrated from Scala to Java: less dependencies.
