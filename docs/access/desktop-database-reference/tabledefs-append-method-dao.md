---
title: TableDefs. Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31eca3f4ca5993a401bd85a4b04299a8697c16e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314378"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="27a8f-102">TableDefs. Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="27a8f-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="27a8f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27a8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27a8f-104">Fügt der **TableDefs**-Auflistung ein neues **TableDef**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="27a8f-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27a8f-105">Syntax</span></span>

<span data-ttu-id="27a8f-106">*Ausdruck* . Append (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="27a8f-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="27a8f-107">*Ausdruck* Eine Variable, die ein **Tabledefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="27a8f-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="27a8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27a8f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27a8f-109">Name</span><span class="sxs-lookup"><span data-stu-id="27a8f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="27a8f-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="27a8f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="27a8f-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="27a8f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="27a8f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27a8f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27a8f-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="27a8f-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="27a8f-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27a8f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="27a8f-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="27a8f-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="27a8f-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="27a8f-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="27a8f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27a8f-117">Remarks</span></span>

<span data-ttu-id="27a8f-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="27a8f-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="27a8f-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="27a8f-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="27a8f-120">Wenn das Objekt, das Sie anfügen, nicht vollständig ist (beispielsweise, wenn Sie keine **Field** -Objekte an eine **Fields** -Auflistung eines **Index** -Objekts angefügt haben, \*\*\*\* bevor es an eine Indexes-Auflistung angefügt wird) oder wenn die Eigenschaften, die in einem oder mehreren festgelegt sind untergeordnete Objekte sind falsch, bei Verwendung der **Append** -Methode wird ein Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="27a8f-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="27a8f-121">Wenn Sie beispielsweise noch keinen Feldtyp angegeben haben und dann versuchen, das **Field** -Objekt an die **Fields** -Auflistung in einem **TableDef** -Objekt anzufügen, löst mithilfe der **Append** -Methode ein Laufzeitfehler aus.</span><span class="sxs-lookup"><span data-stu-id="27a8f-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

