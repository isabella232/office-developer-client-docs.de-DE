---
title: Database.Connection-Eigenschaft (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709838"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="326b8-102">Database.Connection-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="326b8-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="326b8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="326b8-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="326b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="326b8-104">Syntax</span></span>

<span data-ttu-id="326b8-105">*Ausdruck* . Verbindung</span><span class="sxs-lookup"><span data-stu-id="326b8-105">*expression* .Connection</span></span>

<span data-ttu-id="326b8-106">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="326b8-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="326b8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="326b8-107">Remarks</span></span>

<span data-ttu-id="326b8-p101">Rufen Sie mit der **Connection**-Eigenschaft einen Verweis auf das **Connection**-Objekt ab, das dem **Database**-Objekt entspricht. Bei DAO sind ein **Connection**-Objekt und dessen **Database**-Objekt einfach zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Mithilfe der **[Database](connection-database-property-dao.md)** -Eigenschaft eines **Connection**-Objekts und der **Connection**-Eigenschaft eines **Database**-Objekts können Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul leichter zur Verwendung von ODBCDirect geändert werden.</span><span class="sxs-lookup"><span data-stu-id="326b8-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

