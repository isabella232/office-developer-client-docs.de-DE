---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882840"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="60962-102">Database.Connection Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="60962-102">Database.Connection Property (DAO)</span></span>


<span data-ttu-id="60962-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60962-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="60962-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60962-104">Syntax</span></span>

<span data-ttu-id="60962-105">*Ausdruck* . Verbindung</span><span class="sxs-lookup"><span data-stu-id="60962-105">*expression* .Connection</span></span>

<span data-ttu-id="60962-106">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="60962-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="60962-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60962-107">Remarks</span></span>

<span data-ttu-id="60962-p101">Rufen Sie mit der **Connection**-Eigenschaft einen Verweis auf das **Connection**-Objekt ab, das dem **Database**-Objekt entspricht. Bei DAO sind ein **Connection**-Objekt und dessen **Database**-Objekt einfach zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Mithilfe der **[Database](connection-database-property-dao.md)** -Eigenschaft eines **Connection**-Objekts und der **Connection**-Eigenschaft eines **Database**-Objekts können Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul leichter zur Verwendung von ODBCDirect geändert werden.</span><span class="sxs-lookup"><span data-stu-id="60962-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

