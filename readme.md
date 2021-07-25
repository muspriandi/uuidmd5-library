# UUID & MD5 Library
Spring JPA custom strategy generator using UUID and MD5

## Usage

Example for maven project with [JitPack](httpsjitpack.io#jitpackmaven-simple).

Add the following code pom.xml file
```xml
repositories
	repository
		idjitpack.ioid
		urlhttpsjitpack.iourl
	repository
repositories

dependencies
	dependency
		groupIdcom.github.muspriandigroupId
		artifactIduuidmd5-libraryartifactId
		version1.0-SNAPSHOTversion
	dependency

	!-- Other dependencies --
dependencies
```

Use _'com.github.IdGenerator'_ as strategy in modelentity file.
```python
@Id
@GeneratedValue(generator = custom-uuid)
@GenericGenerator(name = custom-uuid, strategy = com.github.IdGenerator)
@Column(name = product_id, insertable = false, updatable = false)
private String productId;
...
```
make sure field(database) is correct, varchar with min. 32 characters or greater.