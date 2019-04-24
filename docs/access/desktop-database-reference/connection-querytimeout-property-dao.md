---
title: Connection. QueryTimeout-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295821"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="d3d60-102">Connection. QueryTimeout-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3d60-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="d3d60-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3d60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3d60-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d3d60-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d60-105">Syntax</span></span>

<span data-ttu-id="d3d60-106">*Ausdruck* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="d3d60-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="d3d60-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3d60-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d60-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3d60-108">Remarks</span></span>

<span data-ttu-id="d3d60-109">Der Standardwert beträgt 60.</span><span class="sxs-lookup"><span data-stu-id="d3d60-109">The default value is 60.</span></span>

<span data-ttu-id="d3d60-p101">Bei einer ODBC-Datenbank, wie z. B. Microsoft SQL Server, können aufgrund des Netzwerkverkehrs oder einer hohen Belastung des ODBC-Servers Verzögerungen auftreten. Um eine unbegrenzte Wartezeit zu vermeiden, können Sie die Zeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3d60-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="d3d60-p102">Wenn Sie **QueryTimeout** mit einem **[Connection](connection-object-dao.md)** - oder **[Database](database-object-dao.md)** -Objekt verwenden, wird ein globaler Wert für alle Abfragen festgelegt, die der Datenbank zugeordnet sind. Sie können diesen Wert für eine bestimmte Abfrage außer Kraft setzen, indem Sie die **ODBCTimeout**-Eigenschaft für das betreffende **[QueryDef](querydef-object-dao.md)** -Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="d3d60-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

