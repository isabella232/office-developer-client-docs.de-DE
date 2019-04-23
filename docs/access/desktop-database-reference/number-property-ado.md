---
title: Number-Eigenschaft (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288574"
---
# <a name="number-property-ado"></a><span data-ttu-id="d77a2-102">Number-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d77a2-102">Number property (ADO)</span></span>


<span data-ttu-id="d77a2-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d77a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d77a2-104">Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d77a2-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d77a2-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d77a2-105">Return value</span></span>

<span data-ttu-id="d77a2-106">Gibt einen **Long**-Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="d77a2-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="d77a2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d77a2-107">Remarks</span></span>

<span data-ttu-id="d77a2-p101">Ermitteln Sie mit der **Number**-Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.</span><span class="sxs-lookup"><span data-stu-id="d77a2-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="d77a2-p102">Die [Errors](errors-collection-ado.md)-Auflistung gibt ein HRESULT im Hexadezimalformat (z. B. 0x80004005) oder einen Long-Wert (beispielsweise 2147467259) zurück. Diese HRESULTs können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Zahlen finden Sie in Kapitel 16 von *OLE DB Programmer's Reference*.</span><span class="sxs-lookup"><span data-stu-id="d77a2-p102">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259). These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself. For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

