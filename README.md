# Database Key Mapper
---
## OPS database
##### 1) ``` user:<user_email> ```
###### return type: &ensp; _hash_  
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
###### return type: &ensp; _hash_  
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
###### return type: &ensp; _hash_  
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
###### return type: &ensp; _hash_  
The keys & descriptions within returned hash  
_Number of Keys will vary based on time span working with client_ 
>

        - <%Y%m> or <YYYYmm>
                return type:    Integer
                description:    Quantifty value

<br> 

##### 2) ``` <abrv>:cat:<cat_name> ```
###### return type: &ensp; _hash_ 
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
###### return type: &ensp; _hash_  
The keys & descriptions within returned hash
>
        
        - "handle"
                return type:
                description:

        - "aspect"
                return type:
                description:

        - "price"
                return type:
                description:

        - "product_url"
                return type:
                description:

        - "image_url"
                return type:
                description:

        - "vendor"
                return type:
                description:

        - "inventory"
                return type:
                description:

        - "category"
                return type:
                description:

        - "inventory_url"
                return type:
                description:

        - "product_id"
                return type:
                description:

        - "inv_tracked"
                return type:    binary value 1 or 0
                description:    If tracked Shopify has data on product's inventory quantities

        - "active"
                return type:    binary value 1 or 0
                description:    If active the product has more than 3 inventory

        - "name"
                return type:    String 
                description:    Name of product

<br>

##### 5) ``` <abrv>:metrics ```
###### return type: &ensp; _hash_  
The keys & descriptions within returned hash
>
   
        - "agg_aov_them"
                return type:
                description:
        - "opened"
                return type:
                description:
        - "aov_us"
                return type:
                description:
        - "agg_itm_them"
                return type:
                description:
        - "avg_viewed_per_session"
                return type:
                description:
                
        - "selected"
                return type:
                description:
                
        - "agg_itm_us"
                return type:
                description:
                
        - "added_to_cart_rate"
                return type:
                description:
                
        - "viewed"
                return type:
                description:
                
        - "checkout"
                return type:
                description:
                
        - "mean_aov"
                return type:
                description:
                
        - "ttl_us"
                return type:
                description:
                
        - "cart"
                return type:
                description:
                
        - "active_modals"
                return type:
                description:
                
        - "ttl_them"
                return type:
                description:
                
        - "mean_itm"
                return type:
                description:
                
        - "checkout_rate"
                return type:
                description:
                
        - "aov_them"
                return type:
                description:
                
        - "avg_opened_per_session"
                return type:
                description:
                
        - "itm_them"
                return type:
                description:
                
        - "agg_aov_us"
                return type:
                description:
                
        - "itm_us"
                return type:
                description:
                
   
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


