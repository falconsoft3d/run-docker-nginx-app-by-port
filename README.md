# How run 3 apps on the same server in diferent port
```
                  +--- host --------> node.js on localhost:8080
                  |
users --> nginx --|--- host/odoo13 ---> odoo on localhost:8181
                  |
                  +--- host/odoo14 ---> odoo on localhost:8181
```
