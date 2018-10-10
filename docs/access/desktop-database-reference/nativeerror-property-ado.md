---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476037"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="d9559-102">NativeError-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d9559-102">NativeError Property (ADO)</span></span>


<span data-ttu-id="d9559-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9559-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9559-104">Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d9559-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9559-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9559-105">Return Value</span></span>

<span data-ttu-id="d9559-106">Gibt einen **Long** -Wert zurück, der den Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="d9559-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9559-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9559-107">Remarks</span></span>

<span data-ttu-id="d9559-p101">Rufen Sie mit der **NativeError** -Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error** -Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError** -Eigenschaft übergeben.</span><span class="sxs-lookup"><span data-stu-id="d9559-p101">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object. For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

