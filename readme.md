# Locale en_CH

## Usefull Linksi: 
- https://askubuntu.com/a/162714/868786
- https://lh.2xlibre.net/locale/en_US/
- https://lh.2xlibre.net/locale/fr_CH/
- https://wiki.ubuntuusers.de/systemd/localectl/
- https://github.com/cbaconnier/ubuntu-locale-en_CH/

- locale definitions for other regions:
    - https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=localedata/locales/en_US
    - https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=localedata/locales/de_DE
    - https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=localedata/locales/de_CH
  
- how to:
    - https://unix.stackexchange.com/questions/348502/why-should-one-use-update-locale-instead-of-directly-setting-language
    - https://unix.stackexchange.com/questions/209853/how-to-easily-be-able-to-use-a-new-en-local

# Installation

tested on debian 11

uncomment `en_US.UTF-8 UTF-8` in `/etc/locale.gen`
add `en_CH UTF-8` to `/etc/locale.gen`


	wget https://raw.githubusercontent.com/meinradr/ubuntu-locale-en_CH/master/en_CH
	# sudo localedef -i en_CH -f UTF-8 en_CH.UTF-8 -c -v
	sudo mv en_CH /usr/share/i18n/locales/
	sudo locale-gen
	sudo localectl set-locale LANG=en_CH.utf-8 LANGUAGE=en_CH:en
	sudo update-locale 
	
Next time you log in, the locale should be in use.

