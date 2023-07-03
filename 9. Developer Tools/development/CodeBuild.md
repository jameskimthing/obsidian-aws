![[CodeBuild.png]]
# CodeBuild
- Build and test code with automatic scaling
- A fully managed continuous integration service that compiles source code, runs tests, and produces ready-to-deploy software packages
- **Configure Environment**
	- Configure the source of the code, such as *github* or [[CodeCommit]]
	- Configure things such as the base OS, or pre-installed packages
- **Configure Execution Steps**
	- Define a *buildspec.yaml* with with execution process details
	- Define build output ("artifacts") details 
	- Run manually / based on triggers
- Can be used alongside [[CodeArtifact]] to get dependencies
