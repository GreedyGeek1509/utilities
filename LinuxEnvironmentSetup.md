
Index
=====
<!--ts-->
   * [Mandatory installations](#mandatory-installs)
   * [Bash Config](#bash-config)
   * [Youtube-DL](#youtube-dl)
   * [Editor Fonts](#editor-fonts)
   * [Sublime Preferences](#sublime-preferences)
<!--te-->


Mandatory Installs
==================
1. Install OpenJDK
    * Java 8 - `sudo apt install openjdk-8-jdk`
    * Java 11 - `sudo apt install openjdk-11-jdk`
2. Install VIM 
    * `sudo apt install vim`
3. [Install git with config](https://linuxize.com/post/how-to-configure-git-username-and-email/)
    * git config --global user.name "Guduri Sriram" 
    * git config --global user.email "email@gmail.com" 
    * git config --global core.editor "vim" 
4. Install maven
    * `sudo apt install maven`
5. Install Docker
    * [Installation walkthrough](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)
    * Add current user to docker group for non sudo execution. (Requires restart) 
    * reconfigure with dns option : Link  
    * DNS option: `/usr/bin/dockerd --dns 10.14.155.200 -H fd:// --containerd=/run/containerd/containerd.sock` 
    * `sudo systemctl daemon-reload`
    * `sudo systemctl restart docker`
6. Install IntelliJ with SNAP
    * Import settings from this [repo](https://github.com/SriramGuduri/utilities/blob/master/settings.zip)
7. Install Brave Browser
8. Install azcli ([Link](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-apt?view=azure-cli-latest)) 
9. Install kubectl
    * `sudo snap install kubectl`
    * configure autocomplete. ([Link](https://kubernetes.io/docs/tasks/tools/install-kubectl/#enabling-shell-autocompletion))
    * install kubectx & kubens ([Link](https://github.com/ahmetb/kubectx))
10. Install helm
11. Install psql client 
    * `sudo apt install postgresql-client-common` 
12. Install pgcli 
    * `sudo apt install pgcli`
    * disable timing conf by setting timing = False in ~/.config/pgcli/config 
13. Install sshpass
    * `sudo apt install sshpass` 
14. Install atom 
15. Install sublime 
16. Install copyq 
    * `sudo apt install copyq`
17. Install terminator
    * `sudo apt install terminator`
18. Install httpie 
    * `sudo apt install httpie`
19. Install fuzzy finder ([link](https://github.com/junegunn/fzf)) 
20. Install sdkman ([link](https://sdkman.io/install)) 
21. Install scala 2.11.7
    * `sdk install scala 2.11.7` 
22. Install spark 2.0.2
    * `sdk install spark 2.0.2` 
23. Install ActivityWatcher ([Link](https://activitywatch.net/)) 
24. Install xclip
    * `sudo apt install xclip`
25. Install pyperclip
    * `sudo pip install pyperclip` 


Bash Config
===========
```bash
# blinking cursor
echo -ne '\e[3 q'

# bash colors
NONE="\[\033[00m\]"
GREEN="\[\033[01;32m\]"
L_CYAN="\[\033[01;36m\]"
BLUE="\[\033[01;34m\]"
YELLOW="\[\033[01;33m\]"
MAGNETA="\[\033[01;35m\]"
export PS1="$GREEN[$L_CYAN\@ $GREEN\u@$YELLOW\h $MAGNETA\W $L_CYAN\$(git branch 2> /dev/null | grep -e '\* ' | sed 's/^..\(.*\)/{\1}/')$GREEN]\$ $NONE"
#end bash colors

#end custom aliases
alias ydl='youtube-dl -f 398+bestaudio --merge-output-format mkv'
alias kctx='kubectx'
alias mvc='mvn clean install'
alias copytoclip='xclip -sel clip <'
alias tcp_dst='sudo tcpdump -A -i wlp3s0 dst'
alias tcp_src='sudo tcpdump -A -i wlp3s0 src'
alias stfu='shutdown now'
alias planner='flatpak run com.github.alainm23.planner'
#end custom aliases
```

Youtube-DL
==========
1. Install youtube-dl
    * [git repo](https://github.com/ytdl-org/youtube-dl)
2. Install ffmpeg
    * `sudo apt install ffmpeg`


Editor Fonts
============
1. Fira Code


Sublime Preferences
===================
```json
{
	"font_face": "Fira Code",
	"font_size": 22,
	"font_options": [
    	"gray_antialias"
	], 
}
```
