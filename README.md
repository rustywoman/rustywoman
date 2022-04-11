### A b o u t

---

> eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJZb3NoaXlhIFdhdGFuYWJlIiwic3ViIjoiUHJvZmlsZSBKV1QiLCJhdWQiOiJQZW9wbGUgd2hvIGFyZSBldmVuIGEgbGl0dGxlIGludGVyZXN0ZWQiLCJuYmYiOjU5OTM1MzIwMCwiaWF0IjoxMzAxNjE2MDAwLCJuaWNrbmFtZSI6InJ1c3R5d29tYW4iLCJsb2NhdGlvbiI6IkphcGFuIiwicm9sZXMiOlsiRW5naW5lZXIiLCJEZXNpZ25lciIsIkNoaWVmIFByaWVzdCIsIkludmVzdG9yIl0sImxhbmd1YWdlcyI6WyJKYXBhbmVzZSIsIkVuZ2xpc2ggKGNvbnZlcnNhdGlvbmFsKSIsIlJ1c3NpYW4gKHN0aWxsIGxlYXJuaW5nKSIsImdvbGFuZyAob3ZlciA1IHllYXJzJyBleHBlcmllbmNlIG9mIHdvcmtpbmcpIiwibm9kZWpzIChvdmVyIDEwIHllYXJzJyBleHBlcmllbmNlIG9mIHdvcmtpbmcpIiwicHl0aG9uIChvdmVyIDEwIHllYXJzJyBleHBlcmllbmNlIG9mIHdvcmtpbmcpIiwiamF2YSAob3ZlciAxNSB5ZWFycycgZXhwZXJpZW5jZSBvZiB3b3JraW5nKSIsImtvdGxpbiAoc3RpbGwgbGVhcm5pbmcpIl0sInBlcnNvbmFsaXR5IjoiSSBhbSBub3QgaGVzaXRhdGUgdG8gZG8gYW55dGhpbmcgdG8gYXR0YWluIG9uZSdzIHB1cnBvc2UuIFRoZXJlZm9yZSwgaXQgb2Z0ZW4gY3JlYXRlcyBoYWxhdGlvbiBpbiB0aGUgb3JnYW5pemF0aW9uLCBidXQgSSByZWFsaXplIGl0IGlzIHVzZWZ1bCBhcyBhIHN0ZXAgdG93YXJkcyByZWZvcm0uIiwiZG9tYWlucyI6WyJodHRwczovL2lsYW1pc29jb2Z5Lm1lLyIsImh0dHBzOi8vbGV0aGUuY28uanAiXX0.SdqeU15aZlSWUr5PEcBiTwYfeGbdHhHQnh7IWiIF7CA

---

If you are interested, please try to analyze the JWT above.

[jwt.io](https://jwt.io/)

<br />

#### P r e p a r a t i o n

---

**OS : Ubuntu ( >= 18.04 )**

[.bashrc](_assets/.bashrc)
[.bash_profile](_assets/.bash_profile)
[.gitconfig](_assets/.gitconfig)
[.tmux.conf](_assets/.tmux.conf)

```sh
# Common
sudo apt-get update
sudo apt-get install \
     apt-transport-https \
     ca-certificates \
     curl \
     gnupg \
     lsb-release \
     make
# Docker
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt update
sudo apt install docker-ce
# Docker-compose ( Latest Version ::: https://docs.docker.com/compose/install/ )
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
# Fish(er)
sudo apt-add-repository ppa:fish-shell/release-2
sudo apt-get update
sudo apt-get install -y fish
curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish
chsh
# Password:
# Changing the login shell for sugi
# Enter the new value, or press ENTER for the default
#         Login Shell [/bin/bash]: /usr/bin/fish
fish install oh-my-fish/theme-bobthefish
string trim '
set -g theme_newline_cursor yes
set -g theme_display_git_master_branch yes
set -g theme_color_scheme dracula
set -g theme_powerline_fonts yes
set -g theme_display_date no
set -g theme_display_cmd_duration no
set -gx LC_ALL en_US.UTF-8
' >> ~/.config/fish/config.fish
# Font for fish (Powerline)
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

---

<br />