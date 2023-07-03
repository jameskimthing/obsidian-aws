#concept 
![[Containers Concept.png]]
- Packages of code and its environment
- Can create so-called *images* which contain container definitions
	- Containers are then instantiated based on images
	- Can be created with software like [Docker](https://www.docker.com)

#### Single Image Application vs. Multi Image Application
- Container(s) contain the parts that make up an application
	- e.g. (1) Web server & database in a single image
	- e.g. (1+) Web server & database in 2 different images
- Scaling
	- Multiple containers, from the same image
	- Multiple containers, from multiple images (+ potential scaling containers)
