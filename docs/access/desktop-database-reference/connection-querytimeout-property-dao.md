---
title: Connection.QueryTimeout Property (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 51f2f51743a8f92b77fafacebbc18e11eb77fe8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473348"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="70924-102">Connection.QueryTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="70924-102">Connection.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="70924-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70924-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="70924-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="70924-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="70924-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70924-105">Syntax</span></span>

<span data-ttu-id="70924-106">*Ausdruck* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="70924-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="70924-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="70924-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="70924-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70924-108">Remarks</span></span>

<span data-ttu-id="70924-109">Der Standardwert beträgt 60.</span><span class="sxs-lookup"><span data-stu-id="70924-109">The default value is 60.</span></span>

<span data-ttu-id="70924-p101">Bei einer ODBC-Datenbank, wie z. B. Microsoft SQL Server, können aufgrund des Netzwerkverkehrs oder einer hohen Belastung des ODBC-Servers Verzögerungen auftreten. Um eine unbegrenzte Wartezeit zu vermeiden, können Sie die Zeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="70924-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="70924-p102">Wenn Sie **QueryTimeout** mit einem **[Connection](connection-object-dao.md)** - oder **[Database](database-object-dao.md)** -Objekt verwenden, wird ein globaler Wert für alle Abfragen festgelegt, die der Datenbank zugeordnet sind. Sie können diesen Wert für eine bestimmte Abfrage außer Kraft setzen, indem Sie die **ODBCTimeout**-Eigenschaft für das betreffende **[QueryDef](querydef-object-dao.md)** -Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="70924-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

