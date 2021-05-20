# Database Key Mapper
---
## OPS database
##### 1) ``` user:<user_email> ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
> 

        - "client"
              return type:      String
              description:      admin or user depending on authorization 
              
        - "email"
              return type:      String with email format
              description:      Email for this employee 

        - "password"
              return type:      String
              description:      Alpha numeric string working as placeholder for account password 

<br>

##### 2) ``` client:<abrv> ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
> 

        - "shopify_key"
                return type:
                description:
                2) "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"
        - "shopify_url"
                return type:    String, url formatting
                description:    The home page url on Shopify for this client

        - "client"
                return type:
                description:
                6) "Golftini"
        - "auth"
                return type:
                description:
                8) "aa7f8449-5d70-4eaf-bf9a-0c4368ce98b7"
        - "shopify_secret"
                return type:
                description:
                10) "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"
        - "inventory"
                return type:    Boolean (python)
                description:    

        - "notes"
                return type:
                description:
                14) "Golftini Wear store"
        - "abrv"
                return type:    String of 4 characters
                description:    The unique id used to refer to all subjects pertaining to this client

<br>

##### 3) ``` 78325bbf-831d-4090-9b46-5c9d54be9b1d ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
> 

        - "client"
                return type:    String
                description:    The company name of this client
                
        - "abrv"
                return type:    String of 4 characters
                description:    The unique id used to refer to all subjects pertaining to this client

        - "auth_id"
                return type:    String formatted as client:<abrv>
                description:
        
        

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
<!-- [viewed, opened, checkout, orders, selected, cart] -->
##### 2) ``` <abrv>:aov ```
##### 2) ``` <abrv>:itm ```

##### 3) ``` <abrv>:ordprod:agg ```
##### 3) ``` <abrv>:<month_id>:billing ```
##### 3) ``` <abrv>:<day_id>:aov ```
##### 3) ``` <abrv>:<day_id>:itm ```
##### 3) ``` <abrv>:<day_id>:orders ```

##### 4) ``` <abrv>:<day_id>:them:aov ```
##### 4) ``` <abrv>:<day_id>:us:aov ```
##### 4) ``` <abrv>:<day_id>:them:itm ```
##### 4) ``` <abrv>:<day_id>:us:itm ```

