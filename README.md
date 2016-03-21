This is a simple test that demonstrates how Hibernate's JPA Metamodel Generator
puts its source files in the wrong place if you're using AspectJ as a compiler.

The case associated with this in the Hibernate bug tracker is at: https://hibernate.atlassian.net/browse/HHH-10626

To demonstrate the problem, simply run:

```mvn compile```

One would expect the generated sources to be under `target/generated-sources/`,
but they are actually placed in the top-level project directory.
