# class18 Reading Notes:Many to many relationships

### Many to many relationships
    
    - @ManyToMany annotation can be used for specifying this type of relationships in Hibernate.

    - Entity Relationship Diagram which shows the many-to-many association between two entities
![](http://hellokoding.com/content/images/2020/11/jpa-guide-2.png)

#### Let's start with a simple Entity Relationship which is the many-to-many association between two entities   employee and project:

employee can be assigned to multiple projects
project may have multiple employees working for it
many-to-many association between the two.

#### Database Setup :
     - reate the employee and project tables along with the employee_project join table with employee_id and project_id.

#### Prepare The model classes Employee and Project need to be created with JPA annotations:

     * Both the Employee class and Project classes refer to one another, which means that the association between     them is bidirectional.

     * In order to map a many-to-many association, we use the @ManyToMany, @JoinTable and @JoinColumn annotations. Let's have a closer look at them.

     * The @ManyToMany annotation is used in both classes to create the many-to-many relationship between the entities.

      *  This association has two sides i.e. the owning side and the inverse side.

       * The @JoinColumn annotation is used to specify the join/linking column with the main table.