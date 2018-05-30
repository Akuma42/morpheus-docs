Blank Dashboard
===============

Problem
  A blank dashboard or 500 error after installing morpheus

.. NOTE:: A blank or 500 error on just the dashboard is different than the entire morpheus-ui not loading. Please see UI note loading article for troubleshooting the ui not loading after an upgrade.

Cause
  Elasticsearch restarting prior to being fully bootstrapped during the initial install.

Solution
  To fix, purge elasticsearch by running the following on the |morpheus| Appliance:

.. code-block:: bash

    curl -XDELETE http://localhost:9200/*
    morpheus-ctl restart elasticsearch
    morpheus-ctl restart morpheus-ui

Another option is:

.. code-block:: bash

  sudo rm –rf /var/opt/|morpheus| /elasticsearch/data/morpheus
  morpheus-ctl restart elasticsearch
  morpheus-ctl restart morpheus-ui

If you get a term/timeout on ui restart, run

.. code-block:: bash

  morpheus-ctl kill morpheus-ui
  morpheus-ctl start morpheus-ui


.. NOTE:: The morpheus-ui may take a few minutes to load and be available after being restarted
