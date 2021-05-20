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
                return type:    String
                description:    Secret key used to Decode message

        - "shopify_url"
                return type:    String, url formatting
                description:    The home page url on Shopify for this client

        - "client"
                return type:    String
                description:    Name of client 

        - "auth"
                return type:    String
                description:    Key used to activate client

        - "shopify_secret"
                return type:    String
                description:    Secret key used to Encode message

        - "inventory"
                return type:    Boolean (python) True or False
                description:    If client has quantities for inventory

        - "notes"
                return type:    String
                description:    Notes referring to client

        - "abrv"
                return type:    String of 4 characters
                description:    The unique id used to refer to all subjects pertaining to this client

<br>

##### 3) ``` <auth> ```
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
                description:    The key used to retrieve the client hash within the ops database
        
        

<br><br>

## DAT database
##### 1) ``` <abrv>:all ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
_Number of Keys will vary based on time span working with client_ 
>

        - <%Y%m> or <YYYYmm>
                return type:    Integer
                description:    Quantifty value

<br> 

##### 2) ``` <abrv>:cat:<cat_name> ```
###### return type: &ensp; _hashset_ 
The keys & descriptions within returned hash
_Number of Keys will vary based on time span working with this category_ 
>  

        - <%Y%m> or <YYYYmm>
                return type:    Integer
                description:    Quantifty value        
           
<br>

##### 3) ``` <abrv>:merch:<product_id> ```
###### return type: &ensp; _list_ 
The keys & descriptions within returned hash
> 

        Returns list of 10 product_id
        List is used to build Prism

<br>

##### 4) ``` <abrv>:prod:<product_id>  ```
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

##### 5) ``` <abrv>:metrics ```
###### return type: &ensp; _hashset_  
The keys & descriptions within returned hash
>
   
        - "agg_aov_them"
                "210.73"
        - "opened"
                4) "[['20210411', 24], ['20210412', 12], ['20210413', 16], ['20210414', 10], ['20210415', 8], ['20210416', 29], ['20210417', 12], ['20210418', 13], ['20210419', 15], ['20210420', 15], ['20210421', 8], ['20210422', 11], ['20210423', 5], ['20210424', 5], ['20210425', 17], ['20210426', 4], ['20210427', 3], ['20210428', 6], ['20210429', 7], ['20210430', 8], ['20210501', 5], ['20210502', 10], ['20210503', 7], ['20210504', 16], ['20210505', 14], ['20210506', 3], ['20210507', 67], ['20210508', 31], ['20210509', 19], ['20210510', 64]]"
        - "aov_us"
                6) "[['20210411', 286.38], ['20210412', 162.0], ['20210415', 88.0], ['20210416', 376.0], ['20210422', 624.0], ['20210423', 192.0], ['20210426', 239.45], ['20210427', 420.48], ['20210428', 524.0]]"
        - "agg_itm_them"
                8) "2.2"
        - "avg_viewed_per_session"
                10) "7.24"
        - "selected"
                12) "[['20210411', 12], ['20210412', 6], ['20210413', 5], ['20210414', 5], ['20210415', 1], ['20210416', 5], ['20210417', 2], ['20210418', 3], ['20210419', 4], ['20210420', 2], ['20210421', 3], ['20210422', 1], ['20210423', 1], ['20210424', 2], ['20210425', 9], ['20210426', 3], ['20210427', 3], ['20210428', 1], ['20210429', 1], ['20210430', 1], ['20210501', 2], ['20210502', 2], ['20210503', 1], ['20210504', 3], ['20210505', 4], ['20210506', 1], ['20210507', 35], ['20210508', 9], ['20210509', 5], ['20210510', 14]]"
        - "agg_itm_us"
                14) "3.39"
        - "added_to_cart_rate"
                16) "18.8"
        - "viewed"
                18) "[['20210411', 125], ['20210412', 96], ['20210413', 22], ['20210414', 28], ['20210415', 23], ['20210416', 55], ['20210417', 43], ['20210418', 42], ['20210419', 34], ['20210420', 24], ['20210421', 36], ['20210422', 44], ['20210423', 11], ['20210424', 16], ['20210425', 8], ['20210426', 9], ['20210427', 2], ['20210428', 12], ['20210429', 18], ['20210430', 35], ['20210501', 9], ['20210502', 25], ['20210503', 13], ['20210504', 33], ['20210505', 27], ['20210506', 12], ['20210507', 71], ['20210508', 37], ['20210509', 28], ['20210510', 141]]"
        - "checkout"
                20) "[['20210411', 6], ['20210412', 1], ['20210413', 0], ['20210414', 0], ['20210415', 2], ['20210416', 9], ['20210417', 3], ['20210418', 2], ['20210419', 0], ['20210420', 3], ['20210421', 0], ['20210422', 3], ['20210423', 3], ['20210424', 0], ['20210425', 0], ['20210426', 3], ['20210427', 2], ['20210428', 3], ['20210429', 0], ['20210430', 0], ['20210501', 2], ['20210502', 0], ['20210503', 2], ['20210504', 1], ['20210505', 0], ['20210506', 0], ['20210507', 1], ['20210508', 1], ['20210509', 7], ['20210510', 7]]"
        - "mean_aov"
                22) "$323.59/$210.73"
        - "ttl_us"
                24) "[['20210411', 572.75], ['20210412', 162.0], ['20210415', 88.0], ['20210416', 376.0], ['20210422', 624.0], ['20210423', 192.0], ['20210426', 478.9], ['20210427', 420.48], ['20210428', 524.0]]"
        - "cart"
                26) "[['20210411', 16], ['20210412', 4], ['20210413', 12], ['20210414', 0], ['20210415', 0], ['20210416', 17], ['20210417', 8], ['20210418', 10], ['20210419', 1], ['20210420', 13], ['20210421', 0], ['20210422', 10], ['20210423', 2], ['20210424', 3], ['20210425', 17], ['20210426', 7], ['20210427', 5], ['20210428', 2], ['20210429', 8], ['20210430', 1], ['20210501', 6], ['20210502', 6], ['20210503', 0], ['20210504', 3], ['20210505', 0], ['20210506', 4], ['20210507', 6], ['20210508', 9], ['20210509', 5], ['20210510', 27]]"
        - "active_modals"
                28) "90"
        - "ttl_them"
                30) "[['20210411', 32752.67], ['20210412', 8165.01], ['20210415', 4430.26], ['20210416', 9098.51], ['20210422', 8921.82], ['20210423', 6286.59], ['20210426', 4143.52], ['20210427', 3150.99], ['20210428', 7581.28]]"
        - "mean_itm"
                32) "3.39/2.20"
        - "checkout_rate"
                34) "5.74"
        - "aov_them"
                36) "[['20210411', 208.62], ['20210412', 240.15], ['20210415', 260.6], ['20210416', 211.59], ['20210422', 207.48], ['20210423', 216.78], ['20210426', 165.74], ['20210427', 175.06], ['20210428', 210.59]]"
        - "avg_opened_per_session"
                38) "1.93"
        - "itm_them"
                40) "[['20210411', 2.32], ['20210412', 2.38], ['20210415', 2.41], ['20210416', 2.3], ['20210422', 2.28], ['20210423', 2.34], ['20210426', 1.64], ['20210427', 1.89], ['20210428', 2.25]]"
        - "agg_aov_us"
                42) "323.59"
        - "itm_us"
                44) "[['20210411', 3], ['20210412', 2], ['20210415', 1], ['20210416', 5], ['20210422', 6], ['20210423', 2], ['20210426', 2.5], ['20210427', 4], ['20210428', 5]]"
   


<br><br>

## MET database
<!--  list of <metric>  [aov, itm] -->
##### 2) ``` <abrv>:<metric> ```

##### 3) ``` <abrv>:ordprod:agg ```

##### 3) ``` <abrv>:<%Y%m>:billing ```

##### 3) ``` <abrv>:<%Y%m%d>:<metric> ```
##### 3) ``` <abrv>:<%Y%m%d>:orders ```

<!-- list of <action>   [viewed, opened, selected, cart, checkout] -->
##### 4) ``` <abrv>:<%Y%m%d>:<session_id>:<action> ```
##### 4) ``` <abrv>:<%Y%m%d>:<session_id>:orders ```

<!--  list of <who>     ['them', 'us'] -->
##### 4) ``` <abrv>:<%Y%m%d>:<who>:<metric> ```


