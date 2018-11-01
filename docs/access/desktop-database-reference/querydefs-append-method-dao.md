---
title: QueryDefs.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c152d52d2a89beaa82061d0d5ae1a5d8d25c1809
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888685"
---
# <a name="querydefsappend-method-dao"></a><span data-ttu-id="47d61-102">QueryDefs.Append Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="47d61-102">QueryDefs.Append Method (DAO)</span></span>


<span data-ttu-id="47d61-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47d61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47d61-104">Fügt der **QueryDefs**-Auflistung ein neues **QueryDef**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="47d61-104">Adds a new **QueryDef** to the **QueryDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47d61-105">Syntax</span></span>

<span data-ttu-id="47d61-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="47d61-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="47d61-107">*Ausdruck* Eine Variable, die ein **QueryDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="47d61-107">*expression* A variable that represents a **QueryDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="47d61-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47d61-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47d61-109">Name</span><span class="sxs-lookup"><span data-stu-id="47d61-109">Name</span></span></p></th>
<th><p><span data-ttu-id="47d61-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="47d61-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="47d61-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="47d61-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="47d61-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47d61-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47d61-113">Objekt</span><span class="sxs-lookup"><span data-stu-id="47d61-113">Object</span></span></p></td>
<td><p><span data-ttu-id="47d61-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47d61-114">Required</span></span></p></td>
<td><p><span data-ttu-id="47d61-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="47d61-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="47d61-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="47d61-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="47d61-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47d61-117">Remarks</span></span>

<span data-ttu-id="47d61-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="47d61-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="47d61-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="47d61-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="47d61-120">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="47d61-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="47d61-121">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="47d61-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

