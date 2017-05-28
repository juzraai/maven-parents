# Maven parent projects

*...to simplify development* 😎



## 1. Usage

### 1.1. Method "A": download and install

1. Download **[the pack](https://github.com/juzraai/maven-parents/archive/master.zip)**
2. Extract the archive
3. Step into the directory
4. Run `mvn install` from terminal
5. Add the desired parent to your project

```xml
<parent>
	<groupId>com.github.juzraai.maven-parents</groupId>
	<artifactId>PARENT-NAME</artifactId>
	<version>VERSION</version> <!-- see .version file in the pack -->
</parent>
```


### 1.2. Method "B": use [JitPack.io](https://jitpack.io/#juzraai/maven-parents)

1. Add JitPack repository to your project

```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
```

2. Add the desired parent to your project

```xml
<parent>
	<groupId>com.github.juzraai.maven-parents</groupId>
	<artifactId>PARENT-NAME</artifactId>
	<version>VERSION</version> <!-- as above or you can specify commit ID too -->
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
