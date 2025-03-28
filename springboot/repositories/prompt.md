Here's the model

```java
public record Activity(UUID id, String name, String description, Instant createdAt){}
```

Help me develop a JPA repository in Spring Boot and Java 21 and follow the below instructions:

1. Write the code as your are senior software engineer who experts in Java and Spring boot with 20 years experience following the best practices and principles.
2. Use Lombok.
3. Use YML on properties
4. Use H2 database
5. Use this as naming convention to an entities: an entity will have `Entity` as suffix. For example: `Activity` as the model then the entity would be `ActivityEntity`
6. Use this as business layer naming convention on model: a model will have the original name. For example: `Activity`
7. Follow the dependency inversion principle where a concret class should depends on interface.
8. A repository name convention will be `JpaActiviyRepository` in `Activity` domain. Please use that as guide.
9. Use `Default` prefix when implementing an interface for example: `ActivityRepository` is an inteface, then the implementation would be `DefaultActivityRepository`.
10. On `ActivityRepository` business layer, use business layer models. Do not use entity class as parameters.
11. On entity class, add a mapping to model. `toModel` when mapping an entity to model then use `fromModel` when mapping model to entity
12. Use Instant on time related fields.
13. Cover these functions only:
    1. save
    2. retrieveById
    3. retrieveAll
    4. delete

## Next prompt

I want further development to add unit testing

1. Cover all possible scenarios: all happy paths and sad paths.
2. Follow this unit test method naming convention <methodName>\_given<>\_then<> for example: on `DefaultActivityRepository`.save then it would be `save_givenValidRecord_thenShouldSave`.
3. Use Mockito on assertions and use AssertJ for complex assertions like asserting a list.
4. Add descriptive message to assertions but be brief and be precise.
5. Just implement a DataJpaTest on business layer for example `DefaultActivityRepository` and do not create explicit test for `JpaRepository`.
6. Assert all the possible fields if there are repetitive assertions, make a utility assert method whenever possible.
7.
