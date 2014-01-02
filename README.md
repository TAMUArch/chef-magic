Magic Cookbook
==============
Chef Cookbook to deploy magic.arch.tamu.edu.  This is a sample site for
a talk about Chef.

To bring up your own test box with Vagrant you need to install Vagrant from
http://www.vagrantup.com and Virtualbox from https://www.virtualbox.org.

Once you have those installed run the following commands:

vagrant plugin install vagrant-berkshelf
vagrant plugin install vagrant-omnibus
vagrant up

You should now have the sample site running on your local box and may view 
it by visiting http://localhost:8080

Requirements
------------

#### cookbooks
- `nginx`
- `git`

Attributes
----------

#### magic::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['magic']['directory']</tt></td>
    <td>String</td>
    <td>Directory to install site to</td>
    <td><tt>/var/www/magic</tt></td>
  </tr>
  <tr>
    <td><tt>['magic']['server_name']</tt></td>
    <td>String</td>
    <td>Directory to install site to</td>
    <td><tt>/var/www/magic</tt></td>
  </tr>
</table>

Usage
-----
#### magic::default

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[magic]"
  ]
}
```

Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write you change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
License: MIT
