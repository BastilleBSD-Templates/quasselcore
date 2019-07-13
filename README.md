# quasselcore
BastilleTemplate to create a Quassel Core Headless IRC Client Jail

 STATUS: Testing

Quassel Core allows you configure an irc server running quassel core that keeps all of your 
connections to your IRC networks live, and you will never miss another message.  It also allows 
you to see logs, etc.

After Quassel Core Jail is up and running you need to configure the IP address for Quassel Core.  
Find the IP address of the jail, then find out you external live IP address on the internet. 

Open Quassel Client and work through the questions to set the IP addresses and IRC networks, etc.
Once done click Save and Connect to connect the core to IRC.



Below is the text output from installing this on freebsd:


	********************************* WARNING *********************************

	FreeBSD does not, and can not warrant that the certification authorities
	whose certificates are included in this package have in any way been
	audited for trustworthiness or RFC 3647 compliance.

	Assessment and verification of trust is the complete responsibility of the
	system administrator.

	*********************************** NOTE **********************************

	This package installs symlinks to support root certificates discovery by
	default for software that uses OpenSSL.

	This enables SSL Certificate Verification by client software without manual
	intervention.

	If you prefer to do this manually, replace the following symlinks with
	either an empty file or your site-local certificate bundle.

	  * /etc/ssl/cert.pem
	  * /usr/local/etc/ssl/cert.pem
	  * /usr/local/openssl/cert.pem

	***************************************************************************
	Message from python36-3.6.9:

	===========================================================================

	Note that some standard Python modules are provided as separate ports
	as they require additional dependencies. They are available as:

	py36-gdbm       databases/py-gdbm@py36
	py36-sqlite3    databases/py-sqlite3@py36
	py36-tkinter    x11-toolkits/py-tkinter@py36

	===========================================================================
	Message from qtchooser-66:

	qtchooser is a wrapper that allows selecting whether Qt4 or Qt5 binaries for
	qmake, moc and other tools will be run when invoking the binaries in $PATH.

	By default, the Qt5 versions are run. It is possible to change the behavior by
	setting the QT_SELECT environment variable to "qt4". See qtchooser(1) for more
	information.
	Message from trousers-0.3.14_2:

	To run tcsd automatically, add the following line to /etc/rc.conf:

	tcsd_enable="YES"

	You might want to edit /usr/local/etc/tcsd.conf to reflect your setup.

	If you want to use tcsd with software TPM emulator, use the following
	configuration in /etc/rc.conf:

	tcsd_enable="YES"
	tcsd_mode="emulator"
	tpmd_enable="YES"

	To use TPM, add your_account to '_tss' group like following:

	# pw groupmod _tss -m your_account
	Message from gnupg-2.2.17:

	***************************************************************************
	GnuPG, when run on hosts without IPv6 connectivity, may fail to connect to
	dual-stack hkp servers [1].  As a workaround, add

	disable-ipv6

	to

	/usr/local/etc/dirmngr.conf

	[1] https://dev.gnupg.org/rGecfc4db3a2f8bc2652ba4ac4de5ca1cd13bfcbec
	***************************************************************************
	Message from qt5-sql-5.12.2:

	======================================================================

	To enable Qt database support, install the database plugin ports. The
	following plugin ports are available:
	 - databases/qt5-sqldrivers-ibase	InterBase/Firebird
	 - databases/qt5-sqldrivers-mysql	MySQL
	 - databases/qt5-sqldrivers-odbc	Open Database Connectivity
	 - databases/qt5-sqldrivers-pgsql	PostgreSQL
	 - databases/qt5-sqldrivers-sqlite2	SQLite 2
	 - databases/qt5-sqldrivers-sqlite3	SQLite 3
	 - databases/qt5-sqldrivers-tds		FreeTDS

	======================================================================
	Message from quassel-core-0.13.0_5:

	=============================================================================
	To run quasselcore at system start-up, add quasselcore_enable="YES"
	to /etc/rc.conf.

	Quassel can use SSL connection between client and core parts. At first start
	quasselcore will ask you to enter some information that will be incorporated
	into generated SSL certificate. You can generate a new certificate by running
	the following command as root:

	# service quasselcore keygen
	or
	# /usr/local/etc/rc.d/quasselcore keygen

	By default quasselcore listens on 4242 port at localhost.
	To change default behavior set quasselcore_args variable in /etc/rc.conf.
	See 'quasselcore --help' for available arguments.
	=============================================================================

