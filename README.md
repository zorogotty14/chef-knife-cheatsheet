# Chef and Knife Commands Cheatsheet

## **Chef Architecture Overview**
Chef follows a **client-server** model with key components:

### **1. Chef Server**
- Stores cookbooks, policies, and metadata.
- Manages nodes and policies.

### **2. Chef Workstation**
- Where developers write cookbooks and recipes.
- Uses `knife` to interact with the Chef Server.

### **3. Chef Client (Node)**
- Runs on managed servers (nodes).
- Pulls configurations from the Chef Server and applies them.

---

## **Common Chef Commands**

### **Managing Chef Workstation**
```sh
chef --version                   # Check installed Chef version
chef generate cookbook <name>    # Create a new cookbook
chef generate recipe <name>      # Create a new recipe
chef generate file <path>        # Create a new file resource
```

### **Uploading Cookbooks**
```sh
knife cookbook upload <name>      # Upload a cookbook to Chef Server
knife cookbook list               # List available cookbooks on the server
knife cookbook delete <name>       # Delete a cookbook from the server
```

### **Managing Nodes**
```sh
knife node list                    # List all nodes
knife node show <node_name>         # Show details of a node
knife node delete <node_name>       # Delete a node
```

### **Managing Roles**
```sh
knife role create <role_name>       # Create a new role
knife role list                      # List all roles
knife role show <role_name>          # Show details of a role
knife role delete <role_name>        # Delete a role
```

### **Managing Environments**
```sh
knife environment list               # List all environments
knife environment show <env_name>    # Show details of an environment
knife environment create <env_name>  # Create a new environment
knife environment delete <env_name>  # Delete an environment
```

### **Managing Data Bags**
```sh
knife data bag create <bag_name>      # Create a data bag
knife data bag list                    # List all data bags
knife data bag show <bag_name>         # Show details of a data bag
knife data bag delete <bag_name>       # Delete a data bag
```

### **Running Chef Client on Nodes**
```sh
chef-client                          # Run Chef on a node
chef-client --local-mode             # Run Chef locally without a server
chef-client -o 'recipe[example]'     # Apply a specific recipe
```

### **Working with Policies**
```sh
chef push policy <policy_name>       # Upload a policy to the Chef Server
chef show policy <policy_name>       # Show policy details
```

---

## **Useful Resources**
- [Chef Official Docs](https://docs.chef.io/)
- [Knife Command Reference](https://docs.chef.io/workstation/knife/)
- [Chef Supermarket](https://supermarket.chef.io/)

---

This cheatsheet provides a quick reference for working with Chef and Knife commands. Let me know if you have any suggestions or improvements!

