# crowdsourcing

This dataset contains records of user task participation, social network relationships, and related fraud detection information. It is designed for analyzing user behavior patterns, social network influences, and task completion outcomes. The data is stored in CSV format and includes 7 files.

### File List and Descriptions

| File Name | Type | Description |
|-----------|------|-------------|
| **final_data_all_with_result.csv** | Master data | The final integrated dataset containing all user task participation information along with outcome labels (e.g., fraud indicator, completion status). |
| **friend.csv** | Social relationship | Friendship connections between users. Typically includes user IDs and their friend IDs, used to construct social network graphs. |
| **msg.csv** | Communication log | Message exchange records between users, possibly containing sender ID, receiver ID, timestamps, etc. |
| **nx_participation_temp.csv** | Intermediate data | Temporary user participation data generated using NetworkX, likely for graph analysis or feature engineering. |
| **nx_task_fraud.csv** | Task fraud | Task-level fraud detection results or features, probably containing task IDs and related fraud metrics. |
| **participation.csv** | Participation record | Core records of user participation in tasks, typically including user ID, task ID, participation time, etc. |
| **task.csv** | Task information | Basic attributes of tasks, such as task name, release time, reward amount, etc. |

### Data Relationships
- **participation.csv** can be linked with **task.csv** via task ID to obtain detailed task information.
- **friend.csv** and **msg.csv** are used to build the user social network, which can be combined with participation records to analyze social influence.
- **final_data_all_with_result.csv** is likely the integrated dataset derived from multiple files, containing the final target variables (e.g., fraud labels).
- Files prefixed with **nx_** are intermediate processing files, typically used for graph algorithm computations or temporary storage.

### Usage Suggestions
1. Start analysis with **final_data_all_with_result.csv**, as it already consolidates key information.
2. To build a user social network graph, use **friend.csv** or **msg.csv**.
3. For task‑level analysis, link **task.csv** with **nx_task_fraud.csv**.
4. It is recommended to use Python’s pandas library for data reading and merging, and NetworkX for social network analysis.

