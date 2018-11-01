---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880180"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="209ab-102">NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="209ab-102">NativeError property (ADO)</span></span>


<span data-ttu-id="209ab-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="209ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="209ab-104">Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="209ab-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="209ab-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="209ab-105">Return value</span></span>

<span data-ttu-id="209ab-106">Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="209ab-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="209ab-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="209ab-107">Remarks</span></span>

<span data-ttu-id="209ab-p101">Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="209ab-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

