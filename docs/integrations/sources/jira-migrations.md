# Jira Migration Guide

## Upgrading to 2.0.0

We're continuously striving to enhance the quality and reliability of our connectors at Airbyte. As part of our commitment to delivering exceptional service, we are transitioning source-jira from the Python Connector Development Kit (CDK) to our innovative low-code framework. This is part of a strategic move to streamline many processes across connectors, bolstering maintainability and freeing us to focus more of our efforts on improving the performance and features of our evolving platform and growing catalog. However, due to differences between the Python and low-code CDKs, this migration constitutes a breaking change.

To gracefully handle these changes for your existing connections, we highly recommend resetting your data before resuming your data syncs with the new version.

1. Select **Connections** in the main navbar.
1.1 Select the connection(s) affected by the update.
2. Select the **Replication** tab.
2.1 Select **Refresh source schema**.
        ```note
        Any detected schema changes will be listed for your review.
        ```
2.2 Select **OK**.
3. Select **Save changes** at the bottom of the page.
3.1 Ensure the **Reset affected streams** option is checked.
        ```note
        Depending on destination type you may not be prompted to reset your data
        ```
4. Select **Save connection**.
        ```note
        This will reset the data in your destination and initiate a fresh sync.
        ```

For more information on resetting your data in Airbyte, see [this page](https://docs.airbyte.com/operator-guides/reset).

## Upgrading to 1.0.0

Note: this change is only breaking if you are using the `Boards Issues` stream in Incremental Sync mode.

This is a breaking change because Stream State for `Boards Issues` will be changed, so please follow the instructions below to migrate to version 1.0.0:

1. Select **Connections** in the main navbar.
   1.1 Select the connection(s) affected by the update.
2. Select the **Replication** tab.
   2.1 Select **Refresh source schema**.
   `note
        Any detected schema changes will be listed for your review.
        `
   2.2 Select **OK**.
3. Select **Save changes** at the bottom of the page.
   3.1 Ensure the **Reset affected streams** option is checked.
   `note
        Depending on destination type you may not be prompted to reset your data
        `
4. Select **Save connection**.
   `note
    This will reset the data in your destination and initiate a fresh sync.
    `

For more information on resetting your data in Airbyte, see [this page](https://docs.airbyte.com/operator-guides/reset).
