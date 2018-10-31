---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a8f324d7216eff2aeeb9045f5c506cdf37170f6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863731"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**Betrifft**: Access 2013 | Office 2013

> [!NOTE]
> [!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.



Bei einem **Connection**-Objekt handelt es sich um eine Verbindung mit einer ODBC-Datenbank (gilt nur für ODBCDirect-Arbeitsbereiche).

## <a name="remarks"></a>Bemerkungen

Ein **Connection**-Objekt ist nicht beständig und stellt eine Verbindung mit einer Remotedatenbank dar. Das **Connection**-Objekt ist nur in ODBCDirect-Arbeitsbereichen verfügbar (d. h. in einem **Workspace**-Objekt, bei dessen Erstellung die Typoption auf **dbUseODBC** festgelegt ist).


> [!NOTE]
> [!HINWEIS] Das **Database**-Objekt kann aus Gründen der Abwärtskompatibilität weiterhin in Code verwendet werden, der für frühere DAO-Versionen geschrieben wurde. Falls Sie jedoch die neuen Features des **Connection**-Objekts erhalten möchten, sollten Sie den Code so überarbeiten, dass das **Connection**-Objekt verwendet wird. Als Hilfestellung bei der Codeumwandlung können Sie einen **Connection**-Objektverweis aus einem **Database**-Objekt abrufen, indem Sie die [Connection](database-connection-property-dao.md)-Eigenschaft des **Database**-Objekts lesen. Umgekehrt erhalten Sie einen **Database**-Objektverweis anhand der **Database**-Eigenschaft des **Connection**-Objekts.


