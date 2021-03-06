.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets. 

|chef server| version 12 is upgraded to |apache solr| 4. If |apache solr| options were added to the |private chef rb| file under ``opscode_solr`` for |chef server oec|, those configuration options are now stored under ``opscode_solr4`` in the |chef server rb| file for |chef server| version 12.

Some ``opscode_solr`` settings are imported automatically, such as heap, new size, and |java| options, but many settings are ignored. If your |chef server oec| configuration is highly tuned for |apache solr|, review `these configuration settings <https://docs.chef.io/config_rb_server_optional_settings.html#opscode-solr4>`__ before re-tuning |apache solr| for |chef server| version 12.
