Generate document for the feature follow example below

## Scheduler

The Scheduler is a feature designed to automate the generation of Reports at specified times and intervals. Users can set up schedules to generate Reports based on predefined Templates, ensuring timely and consistent delivery without manual intervention.

### Key Features of the Scheduler:

-   **Custom Scheduling**: Users can specify the exact time and date for Report generation, including the ability to set recurring schedules. This allows for flexibility and precision in Report delivery.
-   **Cron Syntax Support**: The Scheduler uses cron syntax for defining schedules, providing a powerful and flexible way to specify complex scheduling patterns. Users can enter information such as "2 times a week on Monday and Wednesday at 2pm".
-   **Repeat Intervals**: Users can set up repeated intervals for Report generation, such as daily, weekly, monthly, or custom intervals. This ensures Reports are generated regularly and consistently.

### Functionality:

1. **Schedule Definition**: Allows users to define the schedule for Report generation using cron syntax. The user interface should support easy entry and validation of cron expressions.
2. **Recurring Reports**: Supports the creation of recurring schedules, enabling Reports to be generated at specified intervals without the need for manual triggers.
3. **Notification System**: Sends notifications to users when a Report is generated according to the schedule. Notifications can be sent via email, in-app alerts, or integration with collaboration tools.

### Implementation Details:

-   **Cron Parser**: Develop a parser that interprets cron syntax and translates it into actionable schedules. This parser should handle various cron expressions, including those specifying multiple days, times, and intervals.
-   **User Interface**: Create a user-friendly interface for entering and managing schedules. The interface should provide validation and error-checking for cron expressions to prevent invalid entries.
-   **Notification Mechanism**: Implement a system for sending notifications to users when a Report is generated. This should include options for email notifications, in-app alerts, and integration with tools like Slack or Microsoft Teams.
-   **Database Integration**: Store scheduling information in a database to ensure persistence and reliability. The database should track the next scheduled run time and handle updates to schedules.
-   **Execution Engine**: Build an engine that triggers Report generation based on the defined schedules. This engine should handle the execution of cron jobs and ensure Reports are generated and distributed as specified.
