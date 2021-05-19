# Database Key Mapper
---
## OPS database
##### 1) ``` user:<user_email> ```

##### 2) ``` client:<abrv> ```

##### 3) ``` 78325bbf-831d-4090-9b46-5c9d54be9b1d ```

<br><br>

## DAT database
##### 1) ``` <abrv>:prod:<product_id>  ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
>
        
    - handle:
      return type:
      description:
      
    - aspect
      return type:
      description:
      
    - price
      return type:
      description:
      
    - product_url
      return type:
      description:
      
    - image_url
      return type:
      description:
      
    - vendor
      return type:
      description:
      
    - inventory
      return type:
      description:
      
    - category
      return type:
      description:
      
    - inventory_url
      return type:
      description:
      
    - product_id
      return type:
      description:
      
    - inv_tracked
      return type:    binary value 1 or 0
      description:    If tracked Shopify has data on product's inventory quantities
      
    - active
      return type:    binary value 1 or 0
      description:    If active the product has more than 3 inventory
      
    - name
      return type:    String 
      description:    Name of product

<br>

2) ``` <abrv>:all ```
    - "202104"
    - "21"
    - "202105"
    - "5"

4) ``` <abrv>:cat:<cat_name> ```
    - "202104"
    - "1"

6) ``` <abrv>:merch:<product_id> ```
    - Returns list of 10 product_id

7) ``` <abrv>:metrics ```


<br><br>

## MET database
##### 1) ``` <abrv>:aov ```

##### 2) ``` <abrv>:itm ```

##### 3) ``` <abrv>:ordprod ```

##### 4) ``` <abrv>:somenumber ```


