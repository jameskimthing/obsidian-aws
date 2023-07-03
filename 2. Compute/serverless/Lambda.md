# Serverless Functions
![[Lambda.png]]
- Main [[Serverless]] service
- Can perform tasks in response to events
- Allows you to focus on the code, and not the environment
- *Example:*
	- *Event* (image uploaded) --> *Task* (format image)

#### Usage
- **Code**
	- Upload / define code to be executed
	- Advanced setup (e.g. environment variables)
- **Event**
	- Choose a supported event source
	- Advanced setup (e.g. event filtering)
- **Configuration**
	- Timeout, underlying architecture, file systems, ...
	- Attach execution role for permissions
	- Connect to a [[VPC]] (NOT placed in there though)

