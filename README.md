# Maven parent projects

*...to simplify development* 😎



## 1. Usage

### 1.1. Resolve dependencies

**Method "A": download and install**

1. Download **[the latest release](https://github.com/juzraai/maven-parents/releases/latest)**
2. Extract the archive
3. Step into the directory
4. Run `mvn install` from terminal (root POM will install all parents)

**Method "B": Use [JitPack.io](https://jitpack.io/#juzraai/maven-parents) repository**

1. Just add the repository to your POM or your `settings.xml`

```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```

Here's how to add it globally: [Setting up Multiple Repositories](https://maven.apache.org/guides/mini/guide-multiple-repositories.html)


### 1.2. Reference a parent in your project

Add the desired parent to your project:

```xml
<parent>
	<groupId>com.github.juzraai.maven-parents</groupId>
	<artifactId>PARENT-NAME</artifactId>
	<version>VERSION</version>
</parent>
```



## 2. Common features of all parents

* set source encoding to UTF-8
* suggest versions for some selected dependencies (see pom.xml in root)
* add JitPack repository



## 3. Parents

**kotlin-project**

* turns on Kotlin compiler's incremental option
* adds Kotlin dependencies and JUnit
* adds build plugin for Kotlin, creating JAR and creating JAR with dependencies
* you need to override `main.class` property in your POM



## 4. Versioning

* **Major:** increased on incompatible structural changes
* **Minor:** increased when new feature (e.g. dependency version) added
* **Patch:** increased when I fix a bug or only increase a dependency version



## 5. Contributing

If you find a bug, please open a ticket above.