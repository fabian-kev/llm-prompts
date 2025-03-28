Here's the model

```java
public record Activity(UUID id, String name, String description, Instant createdAt){}
```

Help me develop a JPA repository in Spring Boot and Java 21 and follow the below instructions:

1. Write the code as your are senior software engineer who experts in Java and Spring boot with 20 years experienccce using the best practices and principles.
2. Use maven, and use the latest Spring boot version.
3. Use Lombok.
4. Use YML on properties
5. Use H2 database
6. Use this as naming convention on entity: an entity will have Entity as suffix, for example: MenuItemEntity.
7. Use this as business layer naming convention on model: a model will have the original name, for example: MenuItem.
8. Follow the dependency inversion principle where a concret class should depends on interface.
9. A repository name convention will be JpaMenuItemRepository in MenuItem domain please use that as guide.
10. Use `Default` prefix when implementing an interface for example. MenuItemRepository is an inteface, then the implementation would be DefaultMenuItemRepository.
11. On MenuItemRepository business layer, use business layer models. Do not use entity class as parameters.
12. On entity class, add a mapping to model. toModel when mapping an entity to model then use fromModel when mapping model to entity
13. Use Instant on time related fields.
14. Cover these functions only
    1. save
    2. retrieveById
    3. retrieveAll
    4. delete

## Next prompt

I want further development to add unit testing

1. Add DataJpa testing and cover all possible scenarios
2. Follow this unit test method naming convention <methodName>\_given<>\_then<> for example, on MenuItemService.create it would be create_givenValidMenuItem_thenShouldSave
3. Use Mockito on assertions and use AssertJ for complex assertions like asserting a list
4. Add descriptive message to assertions but be brief.
5. Just implement a DataJpaTest on business layer "DefaultItemMenuRepository" so it's two birds in one stone.
