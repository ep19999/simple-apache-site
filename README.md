# Simple Apache Site

A basic Apache project for deploying a static site using GitHub Actions CI/CD.

This YAML file in this repository allows a GitHub machine to login via SSH to an Amazon EC2 instance,
on which Apache is set to install and start on boot. From here it can serve up the html files with new
commits to the server once a change has been pushed.

The information needed for the SSH connection by Github Actions is contained in Secrets for security.

Only changes in the public-html directory trigger the workflow when pushed to the remote repository as
these are the only files of concern to the apache server.