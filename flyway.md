## Practicing flyway

---

*1. What is Flyway?*

* Flyway is an open source database migration tool. It strongly favors simplicity, conventions over configurations.
* Flyway is developed by boxfuse.
* Flyway can be simply integrated through a dependency.
```
Maven:
<dependency>
   <groupId>org.flywaydb</groupId>
   <artifactId>flyway-core</artifactId>
</dependency>

Gradle:
compile 'org.flywaydb::flyway-core'
```

*Below are some useful commands in flyway*

|Command|What it does|
|-------|------------|
|Migrate| Migrate is the centerpiece of the Flyway workflow. It will scan the filesystem or your classpath for available migrations. It will compare them to the migrations that have been applied to the database. If any difference is found, it will migrate the database to close the gap.|
|Clean|Wipes all your schemas completely clean.|
|Info|Info lets you know where you stand. At a glance you will see which migrations have already been applied, which other ones are still pending, when they were executed and whether they were successful or not.|
|Validate|Validate helps you verify that the migrations applied to the database match the ones available locally.This is very useful to detect accidental changes that may prevent you from reliably recreating the schema.|
|Undo|If target is specified, Flyway will attempt to undo versioned migrations in the order they were applied until it hits one with a version below the target. If group is active, Flyway will attempt to undo all these migrations within a single transaction.|
|Baseline|Baseline is for introducing Flyway to existing databases by baselining them at a specific version. This will cause Migrate to ignore all migrations up to and including the baseline version. Newer migrations will then be applied as usual.|
|Repair|Repairs|
