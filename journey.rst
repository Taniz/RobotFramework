.. code:: robotframework

    *** Settings ***
    Documentation     A resource file with reusable keywords and variables.
    ...               This test is functionally identical to the example in
    ...               valid_login.txt file               
    Suite Setup  Open Browser To Main Page
    #Suite Teardown  Close Browser
    #Test Setup  Go To Main Page
    Resource  resource.txt
    
Primary Actor: Nakki Vene

Other Actor: Jorma Peurala

Role: tester/common user

Introduction
------------------------
Nakki is a normal small sausage who wants to test the login to N4S toolbar site.
Jorma is a normal deer and he is currently studying in JAMK. He is currently on his 3rd year.


User logs in
------------------------
Nakki logs in to the site.

.. code:: robotframework

    *** Test Cases ***
    Open Browser To Main Page
        Open Log In Dialog
        Input Valid Username
        Input Valid Password
        Click Log In

Jorma the helpfull deer notices that Nakki has left himself logged in and kindly logs him out.

.. code:: robotframework
	
	*** Test Casess ***
	Logging out
		Log Out