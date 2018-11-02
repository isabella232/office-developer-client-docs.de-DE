---
title: Database.Connection-Eigenschaft (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927326"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="119ec-102">Database.Connection-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="119ec-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="119ec-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="119ec-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="119ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="119ec-104">Syntax</span></span>

<span data-ttu-id="119ec-105">*Ausdruck* . Verbindung</span><span class="sxs-lookup"><span data-stu-id="119ec-105">*expression* .Connection</span></span>

<span data-ttu-id="119ec-106">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="119ec-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="119ec-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="119ec-107">Remarks</span></span>

<span data-ttu-id="119ec-p101">Rufen Sie mit der **Connection**-Eigenschaft einen Verweis auf das **Connection**-Objekt ab, das dem **Database**-Objekt entspricht. Bei DAO sind ein **Connection**-Objekt und dessen **Database**-Objekt einfach zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Mithilfe der **[Database](connection-database-property-dao.md)** -Eigenschaft eines **Connection**-Objekts und der **Connection**-Eigenschaft eines **Database**-Objekts können Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul leichter zur Verwendung von ODBCDirect geändert werden.</span><span class="sxs-lookup"><span data-stu-id="119ec-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

