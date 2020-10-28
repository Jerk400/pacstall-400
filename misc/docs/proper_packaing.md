### Proper Packaging

---

Read [Proper Pacscript](https://raw.githubusercontent.com/Henryws/pacstall/master/misc/docs/pacscript.md) first.

#### Terminology

$PACKAGE: Your package, generally relating to the GitHub directory (github.com/name/repo/packages/$PACKAGE)

1: don't add version="master". It doesn't have a version number, and it's lazy. Make it semantically versioned.

2: Proper layout of your $PACKAGE directory. It should be something like this:

![](https://github.com/Henryws/pacstall/raw/1.0.4-Celeste/website-images/pacstall_tree.png)

That is to make falling back to a certain version easy.

3: If your PACSCRIPT contains variables, just as the AUR, add an underscore "\_" to the front of the variable in question so there is no confusion.

4: $name and $pkgname are different! $pkgname is the name of the executable to run. $name is generic. The reason behind this is GNOME settings... I'm looking at YOU!

5: Please please please try to package software with make. I found a wrapper for make ([porg](http://porg.sourceforge.net)) that makes it easy to uninstall programs. So try to put an effort to use make rather than anything else