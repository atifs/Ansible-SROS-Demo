# Ansible-SROS-Demo
Example Playbooks for Nokia SROS Routers

## Example 1

Creation of "Customer 10" using NETCONF with ALU R13 BASE YANG modules. XML code is embedded in tasks/main.yml file. Edit-config operation "merge" is used.

```
├── 01_Add_Customer_BASE.yml
└── roles
    ├── nctest01
    │   └── tasks
    │       └── main.yml
```

## Example 2

Creation of "Customer 10" using NETCONF with Nokia YANG modules. XML code is embedded in tasks/main.yml file. Edit-config operation "create" is used.

```
├── 02_Add_Customer_NOKIA.yml
└── roles
    ├── nctest02
    │   └── tasks
    │       └── main.yml
```

## Example 3

Deletion of "Customer 10" using NETCONF with Nokia YANG modules. XML code is contained in separate delete_customer_10.xml file. Edit-config operation "delete" is used.

```
├── 03_Delete_Customer.yml
└── roles
    ├── nctest03
    │   ├── tasks
    │   │   └── main.yml
    │   └── templates
    │       └── delete_customer_10.xml
```

## Example 4

Deletion of "Customer 10" using NETCONF with Nokia YANG modules. XML code is contained in separate remove.xml file. Edit-config operation "remove" is used.

```
├── 04_Remove_Customer.yml
└── roles
    ├── nctest04
    │   ├── tasks
    │   │   └── main.yml
    │   └── templates
    │       └── remove_customer_10.xml
```

## Example 5

Creation of "Customer 10" and a list of VPLS services using NETCONF with Nokia YANG modules. XML code is auto-rendered using the create_vpls.j2 Jinja2 template. VPLS service data is contained in the defaults/main.yml file.

```
├── 05_Create_VPLS_from_Template.yml
└── roles
    └── nctest05
        ├── defaults
        │   └── main.yml
        ├── tasks
        │   └── main.yml
        └── templates
            └── create_vpls.j2
```

