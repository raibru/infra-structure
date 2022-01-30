Ansible Role headless.tools
=========

This role installs some useful tools used in a headless ubuntu environment

##### The list of basic utilities includes:
- **command-not-found**: suggest installation of packages in interactive bash sessions
- **dstat**: tool for generating system resource statistics
- **htop**: interactive process viewer for Linux
- **atop**: another interactive process viewer for Linux
- **smem**: provides numerous reports on memory usage
- **unzip**: tool to unpack zip archives
- **zip**: tool to pack zip archives
- **gzip**: tool to work wih gzip archives
- **bzip2**: tool to work wih bzip2 archives
- **vim**: advanced text editor **Failed on CentOS 5 (already installed as vi)**
- **git**: git distributed version control system, mainly to work with github.com
- **neofetch**: tool to print some highly customizable system info
- **tmux**: tool to use a multiplexer terminal
- **glances**: tool to monitoring and system viewer for Linux 
- **tidy**: tool reads HTML, XHTML and XML files and writes cleaned up markup
- **exuberant-ctags**: build tag file indexes of source code definitions

##### The list of network utilities includes:
- **curl**: command line tool for transferring data with URL syntax
- **iftop**: display bandwidth usage on an interface
- **mtr**: a network diagnostic tool
- **nmap**: Security Scanner For Network Exploration & Hacking
- **wget**: Download manager
- **wget2**: Download manager next generation
- **telnet**: This is telnet
- **iperf**: tool for performing network throughput measurements
- **iperf3**: tool for performing network throughput measurements next generation
- **nuttcp**: another tool for performing network throughput measurements

##### The list of file system utilities includes:
- **iotop**: display io usage on behalf of which process on an interface
- **ncdu**: interactive console disk usage visualizer
- **lsof**: list open files
- **tree**: recursive directory listing program
- **mc**: old file manager

##### The list of developer utilities includes:
- **pstack**: attaches to the active processes named by the pids on the command line , and prints out an execution stack trace
- **strace**: trace system calls and signals
- **ltrace**: library call tracer
- **openjdk-11-jdk**: java jdk
- **cppcheck**: an analysis tool for C/C++ code. It detects possible bugs by rules. Can handle misra rules
- **python3-pip**: pip3 is the official package installer for Python 3.
- **tig**: ncurses-based text-mode interface for git

##### The list of user utilities includes:
- **youtube-dl**: a cli program to download videos from YouTube.com and a few more sites
- **asciidoc**: a text document format for writing notes, documentation, articles, books, man pages and more
- **asciidoctor**: a comprehensive and user-friendly publishing toolchain for the AsciiDoc writing format 
- **graphviz**: a collection of tools for manipulating graph structures and generating graph layouts
- **plantuml**: easily create beautiful UML Diagrams from simple textual description
- **pandoc**: a document converter, widely used as a writing tool and as a basis for publishing workflows
- **taskwarrior**: a cli task list management utility 
- **tasksh**: a tmux configured management tool used with taskwarrior
- **neomutt**: a command line mail reader (or MUA )
- **w3m**: a text-based web browser as well as a pager like `more' or `less'
- **texlive-xetex**: provides a comprehensive TeX system with binaries for most flavors of Unix
- **texlive-fonts-extra**: tex fonts
- **texlive-lang-english**: tex english
- **texlive-lang-german**: tex german
- **librsvg2-bin**: a cli utility to convert SVG files
- **imagemagick**: a suite for displaying, creating, converting, modifying, and editing raster images
- **pdf-presenter-console**: a GTK-based presentation viewer 
- **poppler-utils**: a PDF rendering library based on the xpdf
- **podman**: not yet
- **buildah**: not yet

Requirements
------------

No Requirements

Role Variables
--------------

```yaml
# Role behavior:
utils_install_basic: True               # If set to true role will install basic tools list.
utils_install_network: True             # If set to true role will install network tools list.
utils_install_filesystem: True          # If set to true role will install file system tools list.
utils_install_dev: True                 # If set to true role will install developer tools list.
utils_install_user: True                # If set to true role will install list of user configured packages

# Role lists:
utils_list_basic: []                    # Placeholder for list item. Look at vars/main.yml
utils_list_network: []                  # Placeholder for list item. Look at vars/main.yml
utils_list_filesystem: []               # Placeholder for list item. Look at vars/main.yml
utils_list_dev: []                      # Placeholder for list item. Look at vars/main.yml
utils_list_user: []                     # Placeholder for list item. Look at vars/main.yml

# Apt behavior:
utils_update_cache: True                # If set to true role will update application cache before execution.
utils_upgrade_software: True            # If set to true role will upgrade installed soft
utils_cache_valid: "3600"               # How long cache will be valid after update.
utils_upgrade_type: "safe"              # Default upgrade type. You can use:
                                        # If yes or safe, performs an aptitude safe-upgrade
                                        # If full, performs an aptitude full-upgrade
                                        # If dist, performs an apt-get dist-upgrade
```

Dependencies
------------

Independent role.

Example Playbook
----------------

```yaml
- name: setup extended user tools on headless ubuntu
  hosts: all
  become: true
  roles:
    - headless.tools
```


License
-------

MIT

Author Information
------------------

raibru

