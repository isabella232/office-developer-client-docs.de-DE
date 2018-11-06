---
title: TableDefs.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a0f38d883b39b96eae654fac567fa25b0629e750
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998959"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="a3512-102">TableDefs.Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3512-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="a3512-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3512-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3512-104">Fügt der **TableDefs**-Auflistung ein neues **TableDef**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3512-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3512-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3512-105">Syntax</span></span>

<span data-ttu-id="a3512-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="a3512-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="a3512-107">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3512-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3512-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3512-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3512-109">Name</span><span class="sxs-lookup"><span data-stu-id="a3512-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3512-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="a3512-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a3512-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a3512-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a3512-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3512-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3512-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="a3512-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="a3512-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3512-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3512-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="a3512-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="a3512-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a3512-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3512-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3512-117">Remarks</span></span>

<span data-ttu-id="a3512-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="a3512-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="a3512-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="a3512-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="a3512-120">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="a3512-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="a3512-121">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="a3512-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

