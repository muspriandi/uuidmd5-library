# UUID & MD5 Library
Spring JPA custom strategy generator using UUID and MD5

## Usage

Example for maven project with [JitPack](https://jitpack.io/#jitpack/maven-simple).

Add the following code **pom.xml** file:
```xml
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>

<dependencies>
	<dependency>
		<groupId>com.github.muspriandi</groupId>
		<artifactId>uuidmd5-library</artifactId>
		<version>1.0-SNAPSHOT</version>
	</dependency>

	<!-- Other dependencies -->
</dependencies>
```

Use _'com.github.IdGenerator'_ as strategy in model/entity file.
```python
@Id
@GeneratedValue(generator = "custom-uuid")
@GenericGenerator(name = "custom-uuid", strategy = "com.github.IdGenerator")
@Column(name = "product_id", insertable = false, updatable = false)
private String productId;
...
```
make sure field(database) is correct, **varchar** with min. **32** characters or greater.