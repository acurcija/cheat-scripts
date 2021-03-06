RVM (ruby version manager)
==========================

RVM cheat sheet (official): [http://cheat.errtheblog.com/s/rvm](http://cheat.errtheblog.com/s/rvm)


### Linux

#### Installation

	$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
	  \curl -sSL https://get.rvm.io | bash -s stable --rails

	$ source ~/.rvm/scripts/rvm

### OSX

#### Requirements

Install commmand line tools:

	$ xcode-select --install


#### Installation:

	$ echo "gem: --no-document" >> ~/.gemrc   # do not install gem docs
	$ \curl -sSL https://get.rvm.io | bash -s stable

Add path to bash_profile (if not already there):

    [[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"

Reload the profile: 

    $ source ~/.bash_profile


#### Finding Ruby versions & gems

	$ rvm list
	$ rvm list gemsets
	$ rvm list known

#### Installing Ruby version

	$ su [ADMIN_USER]
	$ rvm install 2.x.x

#### Using Ruby versions

	$ su [ADMIN_USER]
	$ bash --login

	$ rvm use 2.x.x    # use RVM ruby  
	$ rvm system       # fallback to using system installed ruby


#### Remove RVM

	$ sudo rvm implode
	$ sudo rm /etc/rvmrc
	$ gem uninstall rvm

Remove environment variables in bash_profile file
Check to make sure that there are no more variables set: 

	$ env | grep -i rvm

