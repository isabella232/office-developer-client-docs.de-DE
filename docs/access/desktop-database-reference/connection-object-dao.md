---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473448"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**Betrifft**: Access 2013 | Office 2013


> [!NOTE]
> <P>[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</P>



Bei einem **Connection**-Objekt handelt es sich um eine Verbindung mit einer ODBC-Datenbank (gilt nur für ODBCDirect-Arbeitsbereiche).

## <a name="remarks"></a>Bemerkungen

Ein **Connection**-Objekt ist nicht beständig und stellt eine Verbindung mit einer Remotedatenbank dar. Das **Connection**-Objekt ist nur in ODBCDirect-Arbeitsbereichen verfügbar (d. h. in einem **Workspace**-Objekt, bei dessen Erstellung die Typoption auf **dbUseODBC** festgelegt ist).


> [!NOTE]
> <P>[!HINWEIS] Das <STRONG>Database</STRONG>-Objekt kann aus Gründen der Abwärtskompatibilität weiterhin in Code verwendet werden, der für frühere DAO-Versionen geschrieben wurde. Falls Sie jedoch die neuen Features des <STRONG>Connection</STRONG>-Objekts erhalten möchten, sollten Sie den Code so überarbeiten, dass das <STRONG>Connection</STRONG>-Objekt verwendet wird. Als Hilfestellung bei der Codeumwandlung können Sie einen <STRONG>Connection</STRONG>-Objektverweis aus einem <STRONG>Database</STRONG>-Objekt abrufen, indem Sie die <A href="database-connection-property-dao.md">Connection</A>-Eigenschaft des <STRONG>Database</STRONG>-Objekts lesen. Umgekehrt erhalten Sie einen <STRONG>Database</STRONG>-Objektverweis anhand der <STRONG>Database</STRONG>-Eigenschaft des <STRONG>Connection</STRONG>-Objekts.</P>


