.. _JobsJobs:

Jobs
----

.. toggle-header:: :header: Required Role Permissions **Click to Expand/Hide**

    Provisioning: Jobs

    - **None:** Cannot access ``Provisioning > Jobs > Jobs tab``
    - **Read:** Can access ``Provisioning > Jobs > Jobs tab`` but cannot create, edit, or delete Jobs
    - **Full:** Full permissions to create, view, edit, and delete Jobs

    Provisioning: Job Executions

    - **None:** Cannot access ``Provisioning > Jobs > Job Executions tab``
    - **Read:** Can access and view ``Provisioning > Jobs > Job Executions tab`` including job execution history, status, and Job output
|

Creating Jobs
^^^^^^^^^^^^^

.. note:: Jobs require existing Tasks or Workflows. See the appropriate section of |morpheus| docs for more on creating `Tasks <https://docs.morpheusdata.com/en/latest/provisioning/automation/automation.html#tasks>`_ and `Workflows <https://docs.morpheusdata.com/en/latest/provisioning/automation/automation.html#workflows>`_.

To create a new job:

#. Navigate to ``Provisioning > Jobs``
#. Select :guilabel:`+ ADD`
#. Enter the following

   **NAME:** Name of the Job in |morpheus|
   **JOB TYPE:** A Task Job will execute a selected Task, a Workflow Job will execute a selected Workflow
   **ENABLED:** When checked, the Job will run as scheduled

#. Select :guilabel:`NEXT`

#. Configure the Job

   Task Jobs
     **TASK:** Select target Task. If relevant to the Task, Option Type fields will be presented

     **SCHEDULE:**
         Manual: Job is not scheduled but can be executed from ``Provisioning > Jobs`` and selecting ``Actions > Execute``

         Date And Time: Job will be executed at one specific point in time and not again (unless rescheduled or executed manually)

         Schedule: Select a configured Execution Schedule. Execution Schedules are created in ``Provisioning > Automation > EXECUTE SCHEDULING``

         .. note:: |morpheus| provides two default execution schedules, ``Daily at Midnight`` and ``Weekly on Sunday at Midnight``. Any additional schedules were created by a User. Additional schedules can be added in ``Provisioning > Automation > EXECUTE SCHEDULING``

      **CONTEXT TYPE:** Server or Instance

      **CONTEXT SERVER/INSTANCE:** Select the Server or Instance you wish to target with the Job

      **RUN NOW:** When checked, the Job will execute on save regardless of ``SCHEDULE`` setting.

    Workflow Jobs
      **WORKFLOW:** Select target Workflow. If relevant to the Workflow, Option Type fields will be presented

      **SCHEDULE:**
          Manual: Job is not scheduled but can be executed from ``Provisioning > Jobs`` and selecting ``Actions > Execute``

          Date And Time: Job will be executed at one specific point in time and not again (unless rescheduled or executed manually)

          Schedule: Select a configured Execution Schedule. Execution Schedules are created in ``Provisioning > Automation > EXECUTE SCHEDULING``

          .. note:: |morpheus| provides two default execution schedules, ``Daily at Midnight`` and ``Weekly on Sunday at Midnight``. Any additional schedules were created by a User. Additional schedules can be added in ``Provisioning > Automation > EXECUTE SCHEDULING``

      **CONTEXT TYPE:** Server or Instance

      **CONTEXT SERVER/INSTANCE:** Select the Server or Instance you wish to target with the Job

      **RUN NOW:** When checked, the Job will execute on save regardless of ``SCHEDULE`` setting.

#. Select :guilabel:`NEXT`
#. Select :guilabel:`COMPLETE`
