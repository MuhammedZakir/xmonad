# XMonad Maintainers

## The XMonad Core Team

  * Brandon S Allbery [GitHub][geekosaur], IRC: `geekosaur`

  * Brent Yorgey [GitHub][byorgey], IRC: `byorgey`

  * Daniel Wagner [GitHub][dmwit], [Twitter][twitter:dmwit], IRC: `dmwit`

  * Sibi Prabakaran [GitHub][psibi], [Twitter][twitter:psibi], IRC: `sibi`

  * slotThe [GitHub][slotThe], IRC: `Solid`

  * Tomáš Janoušek [GitHub][liskin], [Twitter][twitter:liskin], IRC: `liskin`, [GPG][gpg:liskin]

[geekosaur]: https://github.com/geekosaur
[byorgey]: https://github.com/byorgey
[dmwit]: https://github.com/dmwit
[psibi]: https://github.com/psibi
[liskin]: https://github.com/liskin
[slotThe]: https://github.com/slotThe

[gpg:liskin]: https://github.com/liskin.gpg

[twitter:dmwit]: https://twitter.com/dmwit13
[twitter:psibi]: https://twitter.com/psibi
[twitter:liskin]: https://twitter.com/Liskni_si

## Hall of Fame (past maintainers/developers)

  * Adam Vogt [GitHub](https://github.com/aavogt)

  * Peter Simons [GitHub](https://github.com/peti), [Twitter](https://twitter.com/OriginalPeti)

  * Spencer Janssen [GitHub](https://github.com/spencerjanssen)

  * Don Stewart [GitHub](https://github.com/donsbot), [Twitter](https://twitter.com/donsbot)

  * David Roundy [GitHub](https://github.com/droundy)

  * Daniel Schoepe [GitHub](https://github.com/dschoepe)

  * Eric Mertens [GitHub](https://github.com/glguy)

  * Nicolas Pouillard [GitHub](https://github.com/np)

  * Roman Cheplyaka [GitHub](https://github.com/UnkindPartition)

  * Gwern Branwen [GitHub](https://github.com/gwern)

  * Lukas Mai [GitHub](https://github.com/mauke)

  * Braden Shepherdson [GitHub](https://github.com/shepheb)

  * Devin Mullins [GitHub](https://github.com/twifkak)

  * David Lazar [GitHub](https://github.com/davidlazar)

  * Peter J. Jones [GitHub](https://github.com/pjones)

## Release Procedures

When the time comes to release another version of xmonad and xmonad-contrib:

  1. Update the version number in all the `*.cabal` files and let the CI
     verify that it all builds together.

  2. Review documentation files and make sure they are accurate:

     - [`README.md`](README.md)
     - [`CHANGES.md`](CHANGES.md)
     - [`INSTALL.md`](INSTALL.md)
     - [`man/xmonad.1.markdown.in`](man/xmonad.1.markdown.in)
     - [haddocks](https://xmonad.github.io/xmonad-docs/)

     If the manpage changes, wait for the CI to rebuild the rendered outputs.

  3. Check dependency bounds. In particular, [packdeps][] can be used to check
     if any new versions are excluded by the upper bounds specified.
     Also, make sure that `tested-with:` covers several recent releases of
     GHC, and that `.github/workflows/stack.yml` tests with several recent
     revisions of [Stackage][] LTS.

  4. Create a release on GitHub:

     - https://github.com/xmonad/xmonad/releases/new
     - https://github.com/xmonad/xmonad-contrib/releases/new

     CI will upload a release candidate to Hackage. Check again that
     everything looks good. To publish a final release, run the CI workflow
     once again with the correct version number:

     - https://github.com/xmonad/xmonad/actions/workflows/haskell-ci.yml
     - https://github.com/xmonad/xmonad-contrib/actions/workflows/haskell-ci.yml

     See [haskell-ci-hackage.patch][] for details about the release infrastructure.

  5. Update the website:

     - Post a [new release announcement][web-announce]
     - Check install instructions, guided tour, keybindings cheat sheet, …

  7. Post announcement to:

     - [XMonad mailing list](https://mail.haskell.org/mailman/listinfo/xmonad)
     - [Haskell Cafe](https://mail.haskell.org/cgi-bin/mailman/listinfo/haskell-cafe)
     - [Haskell Discourse](https://discourse.haskell.org/)

     See [old announcements][old-announce] for inspiration.

[packdeps]: https://hackage.haskell.org/package/packdeps
[Stackage]: https://www.stackage.org/
[haskell-ci-hackage.patch]: .github/workflows/haskell-ci-hackage.patch
[web-announce]: https://github.com/xmonad/xmonad-web/tree/gh-pages/news/_posts
[old-announce]: https://github.com/xmonad/xmonad-web/tree/55614349421ebafaef4a47424fcb16efa80ff768

## Website and Other Accounts

* The [xmonad twitter] is tended to by [liskin].

* The [xmonad.org] domain is owned by [eyenx] and the website itself is
  deployed via GitHub Pages.  It can be updated by making a pull request
  against the [xmonad-web] repository.

[eyenx]: https://github.com/eyenx
[xmonad-web]: https://github.com/xmonad/xmonad-web/
[xmonad.org]: https://xmonad.org/
[xmonad twitter]: https://twitter.com/xmonad
