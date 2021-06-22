# code_scanning_demo
This repo demonstrates how to combine multiple code scanning tools using Github Actions and Github Advanced Security.

# Steps to test
1. Fork this repository into your account
2. You will need to enable Actions in this repository. Go to `Actions` tab and click on `I understand my workflows, go ahead and enabled them` button.
3. Even though the workflow exists, you will need to approve it for your repo. On the next screen, select `Org Level Security Checks' workflow.
4. You should see `This scheduled workflow is disabled because scheduled workflows are disabled by default in forks.` warning. Click on `Enable workflow` button next to it.
5. For code scanning to work, Advanced Security needs to have a base scan. Make a minor change to README file and commit to the main branch. This will kick off a scan which you can monitor in Actions tab. Once completed, you'll see a number of vulnerabilities picked up in Security tab.
6. Go ahead, add an insecure code and create a Pull Request.

# Credits
The following repos are leveraged for scanning:
- [terragoat](https://github.com/bridgecrewio/terragoat)
- [dvna](https://github.com/appsecco/dvna)
