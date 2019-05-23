# file encryption using Trezor and GPG
 * install trezor-agent from @romanz  <br>
osx:  `brew install trezor-agent && brew cask install trezor-bridge` <br>
Ubuntu Linux: `apt install trezor/bionic` <br><br>
 * creating GPG keys  <br>
 `trezor-gpg init "Name Surname <name_surname@email.com>"` <br><br>
 * creating aliases to put in ~/.bashrc or ~/.bash_aliases <br>
 `alias encrypt="gpg -e -u 'from_user or email' -r 'to_user or email'" `<br>
 `alias decrypt="gpg -d"` <br> 