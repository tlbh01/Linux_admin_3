#!/bin/bash
# Script to add a user to Linux system
if [ $(id -u) -eq 0 ]; then
    read -p "Enter username : " username
    read -s -p "Enter password : " password
    egrep "^$username" /etc/password >/dev/null
    if [ $? -eq 0 ]; then
        echo "$name exists!"
        exit 1
    else
        pass=$(perl -e 'print crypt($ARGV[0], "password")' $passwd)
        useradd -m -p $pass $username
        [ $? -eq 0 ] && echo "User has been added to system!" || echo "Failed t$
    fi
else
    echo "Only root may add a user to the system"
    exit 2
fi


