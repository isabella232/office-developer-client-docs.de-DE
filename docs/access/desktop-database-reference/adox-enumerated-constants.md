---
title: ADOX-Aufzählungskonstanten
TOCTitle: ADOX enumerated constants
ms:assetid: 0ad716a0-8801-50cb-024a-85c308c65c78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248840(v=office.15)
ms:contentKeyID: 48543163
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 385a3a106c04db11b36ea646368f80fe28ffd413
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720535"
---
# <a name="adox-enumerated-constants"></a><span data-ttu-id="b744d-102">ADOX-Aufzählungskonstanten</span><span class="sxs-lookup"><span data-stu-id="b744d-102">ADOX enumerated constants</span></span>

<span data-ttu-id="b744d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b744d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b744d-p101">Zur Unterstützung des Debugprozesses listen die ADOX-Aufzählungskonstanten einen Wert für jede Konstante auf. Dieser Wert ist jedoch nur eine Empfehlung und kann von einer ADOX­-Version zur anderen variieren. Der Code sollte ausschließlich auf dem Namen, nicht auf dem tatsächlichen Wert der Aufzählungskonstanten basieren.</span><span class="sxs-lookup"><span data-stu-id="b744d-p101">To assist debugging, the ADOX enumerated constants list a value for each constant. However, this value is purely advisory, and may change from one release of ADOX to another. Your code should only depend on the name, not the actual value, of enumerated constants.</span></span>

<span data-ttu-id="b744d-107">Die folgenden Aufzählungskonstanten werden definiert.</span><span class="sxs-lookup"><span data-stu-id="b744d-107">The following enumerated constants are defined.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b744d-108">Aufzählung</span><span class="sxs-lookup"><span data-stu-id="b744d-108">Enumeration</span></span></p></th>
<th><p><span data-ttu-id="b744d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b744d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b744d-110"><a href="actionenum.md">ActionEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-110"><a href="actionenum.md">ActionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-111">Gibt den Aktionstyp an, der beim Aufruf von <strong>SetPermissions</strong> ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b744d-111">Specifies the type of action to be performed when <strong>SetPermissions</strong> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b744d-112"><a href="allownullsenum.md">AllowNullsEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-112"><a href="allownullsenum.md">AllowNullsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-113">Gibt an, ob Datensätze mit Nullwerten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b744d-113">Specifies whether records with null values are indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b744d-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-115">Gibt die Eigenschaften einer <strong>Spalte</strong> an.</span><span class="sxs-lookup"><span data-stu-id="b744d-115">Specifies characteristics of a <strong>Column</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b744d-116"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-116"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-117">Gibt den Datentyp eines <strong>Felds</strong>, eines <strong>Parameters</strong> oder einer <strong>Eigenschaft</strong> an.</span><span class="sxs-lookup"><span data-stu-id="b744d-117">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b744d-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-119">Gibt an, wie Objekte Berechtigungen erben, die mit <strong>SetPermissions</strong> festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b744d-119">Specifies how objects will inherit permissions set with <strong>SetPermissions</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b744d-120"><a href="keytypeenum.md">KeyTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-120"><a href="keytypeenum.md">KeyTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-121">Gibt den Typ des <strong>Schlüssel</strong>-Objekts an: primär, fremd oder eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b744d-121">Specifies the type of <strong>Key</strong>: primary, foreign, or unique.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b744d-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-123">Gibt den Typ des Datenbankobjekts an, für das Berechtigungen oder Besitzrechte festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b744d-123">Specifies the type of database object for which to set permissions or ownership.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b744d-124"><a href="rightsenum.md">RightsEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-124"><a href="rightsenum.md">RightsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-125">Gibt die Rechte oder Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b744d-125">Specifies the rights or permissions for a group or user on an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b744d-126"><a href="ruleenum.md">RuleEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-126"><a href="ruleenum.md">RuleEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-127">Gibt die zu befolgende Regel beim Löschen eines <strong>Key</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b744d-127">Specifies the rule to follow when a <strong>Key</strong> is deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b744d-128"><a href="sortorderenum.md">SortOrderEnum</a></span><span class="sxs-lookup"><span data-stu-id="b744d-128"><a href="sortorderenum.md">SortOrderEnum</a></span></span></p></td>
<td><p><span data-ttu-id="b744d-129">Gibt die Sortierfolge für eine indizierte Spalte an.</span><span class="sxs-lookup"><span data-stu-id="b744d-129">Specifies the sort sequence for an indexed column.</span></span></p></td>
</tr>
</tbody>
</table>

