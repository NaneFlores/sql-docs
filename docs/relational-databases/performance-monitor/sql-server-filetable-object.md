---
title: "SQL Server, FileTable object"
description: "Learn about the SQLServer:FileTable performance object, which provides counters for statistics associated with FileTable and non-transacted access."
author: WilliamDAssafMSFT
ms.author: wiassaf
ms.date: "07/13/2021"
ms.service: sql
ms.subservice: performance
ms.topic: conceptual
helpviewer_keywords:
  - "SQLServer:FileTable"
---
# SQL Server, FileTable object
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
The **SQLServer:FileTable** performance object provides counters for statistics associated with FileTable and non-transacted access.

This following table describes the SQL Server **FileTable** performance objects.

|**SQL Server FileTable counters**|Description|  
|-------------|-----------------|  
|**Avg time delete FileTable item**|Average time (in milliseconds) taken to delete a FileTable item.|
|**Avg time FileTable enumeration**|Average time (in milliseconds) taken for a FileTable enumeration request.|
|**Avg time FileTable handle kill**|Average time (in milliseconds) taken to kill a FileTable handle.|
|**Avg time move FileTable item**|Average time (in milliseconds) taken to move a FileTable item.|
|**Avg time per file I/O request**|Average time (in milliseconds) spent handling an incoming file I/O request.|
|**Avg time per file I/O response**|Average time (in milliseconds) spent handling an outgoing file I/O response.|
|**Avg time rename FileTable item**|Average time (in milliseconds) taken to rename a FileTable item.|
|**Avg time to get FileTable item**|Average time (in milliseconds) taken to retrieve a FileTable item.|
|**Avg time update FileTable item**|Average time (in milliseconds) taken to update a FileTable item.|
|**FileTable db operations/sec**|Total number of database operational events processed by the FileTable store component per second.|
|**FileTable enumeration reqs/sec**|Total number of FileTable enumeration requests per second.|
|**FileTable file I/O requests/sec**|Total number of incoming FileTable file I/O requests per second.|
|**FileTable file I/O response/sec**|Total number of outgoing file I/O responses per second.|
|**FileTable item delete reqs/sec**|Total number of FileTable delete item requests per second.|
|**FileTable item get requests/sec**|Total number of FileTable retrieve item requests per second.|
|**FileTable item move reqs/sec**|Total number of FileTable move item requests per second.|
|**FileTable item rename reqs/sec**|Total number of FileTable rename item requests per second.|
|**FileTable item update reqs/sec**|Total number of FileTable update item requests per second.|
|**FileTable kill handle ops/sec**|Total number of FileTable handle kill operations per second.|
|**FileTable table operations/sec**|Total number of table operational events processed by the FileTable store component per second.|
|**Time delete FileTable item BASE**|For internal use only.|
|**Time FileTable enumeration BASE**|For internal use only.|
|**Time FileTable handle kill BASE**|For internal use only.|
|**Time move FileTable item BASE**|For internal use only.|
|**Time per file I/O request BASE**|For internal use only.|
|**Time per file I/O response BASE**|For internal use only.|
|**Time rename FileTable item BASE**|For internal use only.|
|**Time to get FileTable item BASE**|For internal use only.|
|**Time update FileTable item BASE**|For internal use only.|

## Example

You begin to explore the query performance counters in this object using this T-SQL query on the [sys.dm_os_performance_counters](../system-dynamic-management-views/sys-dm-os-performance-counters-transact-sql.md) dynamic management view:

```sql
SELECT * FROM sys.dm_os_performance_counters
WHERE object_name LIKE '%FileTable%';
```  
 
 
## See also  
[Monitor Resource Usage (System Monitor)](../../relational-databases/performance-monitor/monitor-resource-usage-system-monitor.md)
