.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


An environment is defined using |json| or the |ruby| DSL. |chef solo| will look for environments in ``/var/chef/environments``, but this location can be modified by changing the setting for ``environment_path`` in |solo rb|. For example, the following setting in |solo rb|:

.. code-block:: ruby

   environment_path '/var/chef-solo/environments'

Environment data looks like the following in |json|:

.. code-block:: javascript

   {
     "name": "dev",
     "default_attributes": {
       "apache2": {
         "listen_ports": [
           "80",
           "443"
         ]
       }
     },
     "json_class": "Chef::Environment",
       "description": "",
       "cookbook_versions": {
       "couchdb": "= 11.0.0"
     },
     "chef_type": "environment"
     }

and like the following in the |ruby| DSL:

.. code-block:: ruby

   name 'environment_name'
   description 'environment_description'
   cookbook OR cookbook_versions  'cookbook' OR 'cookbook' => 'cookbook_version'
   default_attributes 'node' => { 'attribute' => [ 'value', 'value', 'etc.' ] }
   override_attributes 'node' => { 'attribute' => [ 'value', 'value', 'etc.' ] }
