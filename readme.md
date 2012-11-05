# Qualtrics R Package

The `qualtrics` R package provides functions to interact with the [Qualtrics](http://www.qualtrics.com) online survey tool. It requires that your account have API access. The latest development version can be installed from Github with the `devtools` package.

	> require(devtools)
	> install_github('qualtrics', 'jbryer')
	
	> ls('package:qualtrics')

Login credentials are required. The `varEntryDialog` provides a user dialog for entering a username and password. Note that although password entry is masked in the dialog, the password is stored in plain text within R.

	> login <- varEntryDialog(vars=c('Username', 'Password'), show=c(NA,'*'))

You can retrieve the list of survey in your account with the `getSurveys` function (note output has been truncated).

	> getSurveys(login$Username, login$Password)