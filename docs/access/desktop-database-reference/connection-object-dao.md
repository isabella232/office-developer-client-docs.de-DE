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
# <a name="connection-object-dao"></a><span data-ttu-id="17084-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="17084-102">Connection Object (DAO)</span></span>


<span data-ttu-id="17084-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17084-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="17084-p101">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17084-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="17084-106">Bei einem **Connection**-Objekt handelt es sich um eine Verbindung mit einer ODBC-Datenbank (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="17084-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="17084-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17084-107">Remarks</span></span>

<span data-ttu-id="17084-p102">Ein **Connection**-Objekt ist nicht beständig und stellt eine Verbindung mit einer Remotedatenbank dar. Das **Connection**-Objekt ist nur in ODBCDirect-Arbeitsbereichen verfügbar (d. h. in einem **Workspace**-Objekt, bei dessen Erstellung die Typoption auf **dbUseODBC** festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="17084-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="17084-p103">[!HINWEIS] Das <STRONG>Database</STRONG>-Objekt kann aus Gründen der Abwärtskompatibilität weiterhin in Code verwendet werden, der für frühere DAO-Versionen geschrieben wurde. Falls Sie jedoch die neuen Features des <STRONG>Connection</STRONG>-Objekts erhalten möchten, sollten Sie den Code so überarbeiten, dass das <STRONG>Connection</STRONG>-Objekt verwendet wird. Als Hilfestellung bei der Codeumwandlung können Sie einen <STRONG>Connection</STRONG>-Objektverweis aus einem <STRONG>Database</STRONG>-Objekt abrufen, indem Sie die <A href="database-connection-property-dao.md">Connection</A>-Eigenschaft des <STRONG>Database</STRONG>-Objekts lesen. Umgekehrt erhalten Sie einen <STRONG>Database</STRONG>-Objektverweis anhand der <STRONG>Database</STRONG>-Eigenschaft des <STRONG>Connection</STRONG>-Objekts.</span><span class="sxs-lookup"><span data-stu-id="17084-p103">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object. To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object. Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>


