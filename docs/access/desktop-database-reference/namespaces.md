---
title: Namespaces (Access PC-Datenbank-Referenz)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703006"
---
# <a name="namespaces"></a><span data-ttu-id="80962-102">Namespaces</span><span class="sxs-lookup"><span data-stu-id="80962-102">Namespaces</span></span>

<span data-ttu-id="80962-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80962-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80962-104">Für das XML-Speicherformat in ADO werden die folgenden vier Namespaces verwendet.</span><span class="sxs-lookup"><span data-stu-id="80962-104">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80962-105">Präfix</span><span class="sxs-lookup"><span data-stu-id="80962-105">Prefix</span></span></p></th>
<th><p><span data-ttu-id="80962-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80962-106">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80962-107">s</span><span class="sxs-lookup"><span data-stu-id="80962-107">s</span></span></p></td>
<td><p><span data-ttu-id="80962-108">Bezieht sich auf die &quot;XML-Daten&quot; Namespace, enthält die Elemente und Attribute, die das Schema des aktuellen <strong>Recordset-Objekt</strong>zu definieren.</span><span class="sxs-lookup"><span data-stu-id="80962-108">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80962-109">dt</span><span class="sxs-lookup"><span data-stu-id="80962-109">dt</span></span></p></td>
<td><p><span data-ttu-id="80962-110">Die Spezifikation für die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="80962-110">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80962-111">rs</span><span class="sxs-lookup"><span data-stu-id="80962-111">rs</span></span></p></td>
<td><p><span data-ttu-id="80962-112">Der Namespace, der die Elemente und Attribute speziell für die ADO-Eigenschaften und -Attribute des <strong>Recordset</strong>-Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="80962-112">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80962-113">z</span><span class="sxs-lookup"><span data-stu-id="80962-113">z</span></span></p></td>
<td><p><span data-ttu-id="80962-114">Das Schema des aktuellen Rowsets.</span><span class="sxs-lookup"><span data-stu-id="80962-114">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80962-115">Ein Client sollten nicht auf diese Namespaces eigenen Tags hinzufügen, gemäß der Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="80962-115">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="80962-116">Beispielsweise sollte ein Client nicht als einen Namespace definieren "Urn: Schemas-Microsoft-Com:rowset", und klicken Sie dann schreiben Sie etwas wie "Rs: MyOwnTag."</span><span class="sxs-lookup"><span data-stu-id="80962-116">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="80962-117">Weitere Informationen zu Namespaces finden Sie unter [XML-Namespaces](https://www.w3.org/tr/xml-names/).</span><span class="sxs-lookup"><span data-stu-id="80962-117">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>

> [!NOTE]
> <span data-ttu-id="80962-118">[!HINWEIS] Die ID für das Schematag muss "RowsetSchema" lauten, und der Namespace, mit dem auf das Schema des aktuellen Rowsets verwiesen wird, muss auf "#RowsetSchema" zeigen.</span><span class="sxs-lookup"><span data-stu-id="80962-118">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span>

<span data-ttu-id="80962-119">Beachten Sie, dass Sie ein beliebiges Präfix für den Namespace verwenden können, also das Element rechts vom Doppelpunkt und links vom Gleichheitszeichen.</span><span class="sxs-lookup"><span data-stu-id="80962-119">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="80962-p102">Der Benutzer kann hierfür einen beliebigen Namen definieren, vorausgesetzt dieser Name wird im gesamten XML-Dokument einheitlich verwendet. ADO gibt "s", "rs", "dt", und "z" immer aus, aber diese Präfixnamen sind in der ladenden Komponente nicht hartcodiert.</span><span class="sxs-lookup"><span data-stu-id="80962-p102">The user can define this to be any name as long as this name is consistently used throughout the XML document. ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>



