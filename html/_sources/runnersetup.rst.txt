************************************
Setting up the CI Runner for Gitlab
************************************


CI is Continuous intergration.  Allows multiple people to work on the same project code in real time.  Users create code,
and upload/merge to the CI server many times throughout the workday. We are going to use a mac OS runner with our Gitlab server.

.. note:: Install the runner on a different host than your GitLab server.

#.
  Using terminal, download the binary package.

  ``sudo curl --output /usr/local/bin/gitlab-runner https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-darwin-amd64``
#.
  Make the binary executable.

  ``sudo chmod +x /usr/local/bin/gitlab-runner``

**The following commands need to be run as the user that's going to run the runner.**

Install & Register the runner
-----------------------------

Registering the runner binds the runner to your gitlab server. Make sure you install the runner on a different server than gitlab.
You can only add the runner to your gitlab server if you are the admin of the GitLab server.
Change to your home dir, `install <https://docs.gitlab.com/runner/install/osx.html#installation>`_ the runner and start the service.

  - ``cd ~``

  - ``gitlab-runner install``

  - ``gitlab-runner start``


The registration token is available at the ``admin/runners`` page.

.. image:: _static/images/runnertoken.png

**Register**

- ``gitlab-runner register``

- Enter your Gitlab server url.
- ``https://my.server.com``
- Enter your runner token.
- ``myS3crT0k``
- Enter a description for the runner.  If you can't think of anything clever, it can be changed later in the UI.
- Next enter tags for the runner. Add as many as you would like, separated by commas.
- Enter the runner executor, we used ``docker``
- Lastly we need to set the default image docker will use to build the envirnoment.  We are using ``alpine:latest`` or alpine 3.6.

For other configurations and OS's check out `Gitlab's Registering Runners Documentation <https://docs.gitlab.com/runner/register/index.html>`_.
