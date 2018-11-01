---
title: Number-Eigenschaft (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72afba54062a3f103fe75939502c9f52eef4c44d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887197"
---
# <a name="number-property-ado"></a><span data-ttu-id="45e85-102">Number-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="45e85-102">Number property (ADO)</span></span>


<span data-ttu-id="45e85-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45e85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45e85-104">Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="45e85-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="45e85-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45e85-105">Return value</span></span>

<span data-ttu-id="45e85-106">Gibt einen **Long** -Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="45e85-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="45e85-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45e85-107">Remarks</span></span>

<span data-ttu-id="45e85-p101">Ermitteln Sie mit der **Number** -Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.</span><span class="sxs-lookup"><span data-stu-id="45e85-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="45e85-110">Die [Errors](errors-collection-ado.md) -Auflistung gibt ein HRESULT im Hexadezimal-Format (beispielsweise 0 x 80004005) oder long-Wert (beispielsweise 2147467259) zurück.</span><span class="sxs-lookup"><span data-stu-id="45e85-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="45e85-111">Diese HRESULT-Werte können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="45e85-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="45e85-112">Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*</span><span class="sxs-lookup"><span data-stu-id="45e85-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

