---
title: SQLState-Eigenschaft (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb4a9adbc6060b7c33e128a0a3fca8c1eb7bc10d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716299"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="75833-102">SQLState-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="75833-102">SQLState property (ADO)</span></span>


<span data-ttu-id="75833-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75833-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75833-104">Gibt den SQL-Status für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75833-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="75833-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75833-105">Return value</span></span>

<span data-ttu-id="75833-106">Gibt einen aus fünf Zeichen bestehenden **String** -Wert zurück, der dem ANSI SQL-Standard entspricht und einen Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="75833-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75833-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75833-107">Remarks</span></span>

<span data-ttu-id="75833-p101">Verwenden Sie die **SQLState** -Eigenschaft, um den aus fünf Zeichen bestehenden Fehlercode zu lesen, der vom Anbieter im Falle eines Fehlers bei der Verarbeitung einer SQL-Anweisung zurückgegeben wird. Wenn Sie z. B. den Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwenden, stammen SQL-Statusfehlercodes von ODBC. Die Codes basieren entweder auf Fehlern, die nur für ODBC gelten, oder auf Fehlern, die von Microsoft SQL Server stammen und dann ODBC-Fehlern zugeordnet wurden. Dieses Fehlercodes sind im ANSI SQL-Standard dokumentiert, sind jedoch in verschiedenen Datenquellen möglicherweise unterschiedlich implementiert.</span><span class="sxs-lookup"><span data-stu-id="75833-p101">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement. For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors. These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

