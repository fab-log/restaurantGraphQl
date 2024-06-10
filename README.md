# restaurantGraphQl
This repo was part of an exercise in the MIT xPRO full stack developer course. It uses multiple graphQL statements for different CRUD operations in a small hardcoded data base.

In order to run this application copy the code, open a terminal, navigate to the folder in which the code was saved and execute the following commands
- npm init
- npm i
- node index.js

Now open a browser and enter this adress: http://localhost:5500/graphql

In the left pane you can copy these statements:

        mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
          editrestaurant(id: $idd, name: $name) {
            name
            description
          }
        }
        
        mutation setrestaurants {
          setrestaurant(input: {
            name: "Granite",
            description: "American",
          }) {
            name
            description
          }
        }
        
        mutation deleterestaurants($iid: Int = 1) {
          deleterestaurant(id: $iid) {
            ok
          }
        }
        
        query getrestaurant($iid: Int = 1) {
          restaurant(id:$iid) {
            name
            description
          }
        }
        
        query getrestaurants {
          restaurants {
            name
            description
            dishes {
              name
              price
            }
          }
        }
