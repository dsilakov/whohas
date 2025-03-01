# Notes for whohas

More information can be found at http://www.philippwesche.org/200811/whohas/intro.html

Philipp L. Wesche

whohas is a command line tool that allows querying several package lists at once - currently supported are Arch, Debian, Gentoo and Slackware. whohas is written in Perl and was designed to help package maintainers find ebuilds, pkgbuilds and similar package definitions from other distributions to learn from. However, it can also be used by normal users who want to know:
- Which distribution has packages available for apps upon whom the user depends.
- What version of a given package is in use in each distribution, or in each release of a distribution (implemented only for Debian).

whohas gives urls to more details about the package. I recommend using a terminal that recognises hyperlinks and allows easy forwarding to the browser.

You can use grep to improve your search results:
```
whohas gimp | grep "gimp "
```
The space will ensure that only results for the package gimp are displayed, not for gimp-print etc.
```
whohas gimp | grep Arch
whohas gimp | grep -i arch
```
Either one of the above will display results for Arch Linux only. If you are interested in the search term or package arch, and want results for Arch Linux only,
```
whohas arch | grep "^Arch"
```

Example output:
```
[phil@epistasis whohas_release]$ whohas gaim
Arch      gaim                      1.4.0-1    10-07-2005 Current     http://www.archlinux.org/packages.php?id=4226
Arch      gaim-encryption           2.38-1     14-06-2005 Extra       http://www.archlinux.org/packages.php?id=5518
Arch      festival-gaim             1.1-1                 community   http://aur.archlinux.org/packages.php?do_Details=1&ID=1017
Arch      gaim-latex                0.3-1                 unsupported http://aur.archlinux.org/packages.php?do_Details=1&ID=1058
Arch      gaim-otr                  2.0.2-1               unsupported http://aur.archlinux.org/packages.php?do_Details=1&ID=1242
Arch      gaim-xmms                 0.33-1                unsupported http://aur.archlinux.org/packages.php?do_Details=1&ID=121
Arch      guifications              2.9-1                 unsupported http://aur.archlinux.org/packages.php?do_Details=1&ID=640
Debian    gaim                      1                     oldstable   http://packages.debian.org/oldstable/net/gaim
Debian    gaim                      1                     stable      http://packages.debian.org/stable/net/gaim
Debian    gaim                      1                     testing     http://packages.debian.org/testing/net/gaim
Debian    gaim                      1                     unstable    http://packages.debian.org/unstable/net/gaim
Debian    gaim-autoprofile          2.10-1                testing     http://packages.debian.org/testing/net/gaim-autoprofileDebian    gaim-autoprofile          2.10-2                unstable    http://packages.debian.org/unstable/net/gaim-autoprofile
Debian    gaim-common               1                     oldstable   http://packages.debian.org/oldstable/net/gaim-common
Debian    gaim-data                 1                     stable      http://packages.debian.org/stable/net/gaim-data
Debian    gaim-data                 1                     testing     http://packages.debian.org/testing/net/gaim-data
Debian    gaim-data                 1                     unstable    http://packages.debian.org/unstable/net/gaim-data
Debian    gaim-dev                  1                     stable      http://packages.debian.org/stable/devel/gaim-dev
Debian    gaim-dev                  1                     testing     http://packages.debian.org/testing/devel/gaim-dev
Debian    gaim-dev                  1                     unstable    http://packages.debian.org/unstable/devel/gaim-dev
Debian    gaim-encryption           2.36-3                stable      http://packages.debian.org/stable/net/gaim-encryption
Debian    gaim-encryption           2.37-1                testing     http://packages.debian.org/testing/net/gaim-encryption
Debian    gaim-encryption           2.38-1                unstable    http://packages.debian.org/unstable/net/gaim-encryptionDebian    gaim-extendedprefs        0.4-4                 stable      http://packages.debian.org/stable/net/gaim-extendedprefs
Debian    gaim-extendedprefs        0.4-4                 testing     http://packages.debian.org/testing/net/gaim-extendedprefs
Debian    gaim-extendedprefs        0.4-6                 unstable    http://packages.debian.org/unstable/net/gaim-extendedprefs
Debian    gaim-gnome                1                     oldstable   http://packages.debian.org/oldstable/net/gaim-gnome
Debian    gaim-guifications         2.10-1                stable      http://packages.debian.org/stable/net/gaim-guificationsDebian    gaim-guifications         2.10-1                testing     http://packages.debian.org/testing/net/gaim-guifications
Debian    gaim-guifications         2.10-1                unstable    http://packages.debian.org/unstable/net/gaim-guifications
Debian    gaim-meanwhile            1.2.3-1               testing     http://packages.debian.org/testing/net/gaim-meanwhile
Debian    gaim-meanwhile            1.2.3-1               unstable    http://packages.debian.org/unstable/net/gaim-meanwhile
Debian    gaim-otr                  2.0.1-1               stable      http://packages.debian.org/stable/net/gaim-otr
Debian    gaim-otr                  2.0.2-1               testing     http://packages.debian.org/testing/net/gaim-otr
Debian    gaim-otr                  2.0.2-1               unstable    http://packages.debian.org/unstable/net/gaim-otr
Debian    gaim-themes               0.1-1                 stable      http://packages.debian.org/stable/net/gaim-themes
Debian    gaim-themes               0.1-1                 testing     http://packages.debian.org/testing/net/gaim-themes
Debian    gaim-themes               0.1-1                 unstable    http://packages.debian.org/unstable/net/gaim-themes
Gentoo    gaim-blogger              1.0.0      22-03-2005             http://packages.gentoo.org/ebuilds/?gaim-blogger-1.0.0
Gentoo    gaim-bnet                 0.1.1      04-03-2005             http://packages.gentoo.org/ebuilds/?gaim-bnet-0.1.1
Gentoo    gaim-bnet                 0.1.0      17-02-2005             http://packages.gentoo.org/ebuilds/?gaim-bnet-0.1.0
Gentoo    gaim-meanwhile            1.2.3      14-06-2005             http://packages.gentoo.org/ebuilds/?gaim-meanwhile-1.2.3
Gentoo    gaim-meanwhile            1.2.2      04-05-2005             http://packages.gentoo.org/ebuilds/?gaim-meanwhile-1.2.2
Gentoo    gaim-meanwhile            1.2.0      10-04-2005             http://packages.gentoo.org/ebuilds/?gaim-meanwhile-1.2.0
Gentoo    gaim-meanwhile            1.0.2      08-02-2005             http://packages.gentoo.org/ebuilds/?gaim-meanwhile-1.0.2
Gentoo    gaim-snpp                 0.8.0      21-02-2005             http://packages.gentoo.org/ebuilds/?gaim-snpp-0.8.0
Gentoo    gaim-assistant            0.09       06-01-2005             http://packages.gentoo.org/ebuilds/?gaim-assistant-0.09Gentoo    gaim-assistant            0.07       06-01-2005             http://packages.gentoo.org/ebuilds/?gaim-assistant-0.07Gentoo    gaim-encryption           2.38       12-07-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.38
Gentoo    gaim-encryption           2.37       13-05-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.37
Gentoo    gaim-encryption           2.36       07-07-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.36
Gentoo    gaim-encryption           2.35       27-02-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.35
Gentoo    gaim-encryption           2.34       24-01-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.34
Gentoo    gaim-encryption           2.32-r1    07-02-2005             http://packages.gentoo.org/ebuilds/?gaim-encryption-2.32-r1
Gentoo    gaim-extprefs             0.4-r1     04-06-2005             http://packages.gentoo.org/ebuilds/?gaim-extprefs-0.4-r1
Gentoo    gaim-extprefs             0.4        30-03-2005             http://packages.gentoo.org/ebuilds/?gaim-extprefs-0.4
Gentoo    gaim-latex                0.3        17-06-2005             http://packages.gentoo.org/ebuilds/?gaim-latex-0.3
Gentoo    gaim-otr                  2.0.2      17-05-2005             http://packages.gentoo.org/ebuilds/?gaim-otr-2.0.2
Gentoo    gaim-otr                  2.0.1      30-03-2005             http://packages.gentoo.org/ebuilds/?gaim-otr-2.0.1
Gentoo    gaim-otr                  2.0.0      10-02-2005             http://packages.gentoo.org/ebuilds/?gaim-otr-2.0.0
Gentoo    gaim-otr                  1.0.3      09-02-2005             http://packages.gentoo.org/ebuilds/?gaim-otr-1.0.3
Gentoo    gaim-rhythmbox            1.0.0.1    21-10-2004             http://packages.gentoo.org/ebuilds/?gaim-rhythmbox-1.0.0.1
Gentoo    gaim-xmms-remote          1.8        29-10-2004             http://packages.gentoo.org/ebuilds/?gaim-xmms-remote-1.8
Gentoo    gaim-xmms-remote          1.7        21-10-2004             http://packages.gentoo.org/ebuilds/?gaim-xmms-remote-1.7
Gentoo    gaimosd                   1.0.0      18-02-2005             http://packages.gentoo.org/ebuilds/?gaimosd-1.0.0
Gentoo    gaim-smileys              20031002   24-06-2004             http://packages.gentoo.org/ebuilds/?gaim-smileys-20031002
Gentoo    autoprofile               2.10       21-10-2004             http://packages.gentoo.org/ebuilds/?autoprofile-2.10
Gentoo    bangexec                  1.3.0.2    21-06-2005             http://packages.gentoo.org/ebuilds/?bangexec-1.3.0.2
Gentoo    bangexec                  1.3.0      21-04-2005             http://packages.gentoo.org/ebuilds/?bangexec-1.3.0
Gentoo    bangexec                  1.1.4      03-04-2005             http://packages.gentoo.org/ebuilds/?bangexec-1.1.4
Gentoo    guifications              2.10       10-04-2005             http://packages.gentoo.org/ebuilds/?guifications-2.10
Gentoo    guifications              2.9        11-02-2005             http://packages.gentoo.org/ebuilds/?guifications-2.9
Gentoo    guifications              2.8        07-02-2005             http://packages.gentoo.org/ebuilds/?guifications-2.8
Gentoo    ignorance                 1.3.1.2    13-07-2005             http://packages.gentoo.org/ebuilds/?ignorance-1.3.1.2
Gentoo    ignorance                 1.3.0      21-04-2005             http://packages.gentoo.org/ebuilds/?ignorance-1.3.0
Slackware gaim                      1.4.0-i486            slackware
```

The first column is the name of the distribution, the second the name of the package, the third the version number, then the date, repository name and a url linking to more information about the package. Future versions will have package size information, too. Column lengths are fixed, so you can use cut:
```
whohas vim | grep " vim " | cut -b 36-45
```

The first bytes of the data fields at the time of writing are 11, 37, 48, 59 and 71.

I would like to encourage distributors at this time to provide web query interfaces to package lists, and specifically provide the following information: package name, version, date, size and a url to further information (maintainer, build information etc.)

Additional remarks: Debian refers to the binary distribution. Slackware queries Current only. All details (including availability, version numbers and binary sizes) are for the x86 architecture, although this cannot be assured for either Debian or Gentoo in the current version of whohas. I recommend you consult the URLs provided in the output.

Bug reports may be sent to phi1ipp@yahoo.com.



## Related software

Repology is an open source service to track versions in distros:

https://repology.org/

pkgs.org is a service for searching Linux/BSD package repositories:

https://pkgs.org/

namecheck is a tool from Debian devscripts to check where names are used:

https://manpages.debian.org/namecheck
