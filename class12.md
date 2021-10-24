# class12 Reading Notes:

## Spring RequestMapping:
![Spring RequestMapping](https://i2.wp.com/springframework.guru/wp-content/uploads/2017/09/mvc.png)

1. RequestMapping — by Path:
2. equestMapping — the HTTP Method(it hasnt defaul value).

B. RequestMapping and HTTP Headers:

    1. RequestMapping With the headers Attribute.
    2. RequestMapping Consumes and Produces.

C. RequestMapping With Path Variables:
   
    1. Single @PathVariable.
    2. Multiple @PathVariable.
    3. @PathVariable With Regex

D. RequestMapping With Request Parameters.

E. RequestMapping Corner Cases
    1. @RequestMapping — Multiple Paths Mapped to the Same Controller Method.
    2. @RequestMapping — Multiple HTTP Request Methods to the Same Controller Method.
    3. @RequestMapping — a Fallback for All Requests.
    4.  Ambiguous Mapping Error (when Spring evaluates two or more request mappings to be the same for different controller methods).

F. New Request Mapping Shortcuts:

- This improve the readability and reduce the verbosity of the code.

    1. @GetMapping.
    2. @PostMapping
    3. @PutMapping
    4. @DeleteMapping
    5. @PatchMapping


## Baeldung: Comparing repositories:

### Spring Data Repositories:
![CRUD Repo](https://ozenero.com/wp-content/uploads/2021/05/Overview-How-to-Integrate-Springboot-2.x-with-MSSQL-using-Spring-JPA.png)

   1. CrudRepository provides CRUD functions.
      * CRUD functionality(save()) ,findone,indAll,count ,delete ,exist)
      


   2. PagingAndSortingRepository(Sort records).
       * It extends CRUD repository
   3. JpaRepository (flushing the persistence context and delete records).

   * Can use each of them independently.
    