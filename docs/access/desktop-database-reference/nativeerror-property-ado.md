---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705946"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="2652c-102">NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2652c-102">NativeError property (ADO)</span></span>


<span data-ttu-id="2652c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2652c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2652c-104">Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2652c-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="2652c-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2652c-105">Return value</span></span>

<span data-ttu-id="2652c-106">Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="2652c-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2652c-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2652c-107">Remarks</span></span>

<span data-ttu-id="2652c-p101">Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="2652c-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

