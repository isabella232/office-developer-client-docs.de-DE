---
title: RowMap-Element (DataRecordSet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Ordnet eine Datensatzgruppe-Zeile einem Shape zu.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332515"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="d4805-103">RowMap-Element (DataRecordSet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d4805-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d4805-104">Ordnet eine Datensatzgruppe-Zeile einem Shape zu.</span><span class="sxs-lookup"><span data-stu-id="d4805-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4805-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d4805-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4805-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="d4805-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d4805-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="d4805-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d4805-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d4805-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d4805-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d4805-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d4805-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d4805-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d4805-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="d4805-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d4805-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="d4805-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4805-113">Definition</span><span class="sxs-lookup"><span data-stu-id="d4805-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d4805-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d4805-114">Elements and attributes</span></span>

<span data-ttu-id="d4805-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d4805-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d4805-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4805-116">Parent elements</span></span>

****

|<span data-ttu-id="d4805-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4805-117">**Element**</span></span>|<span data-ttu-id="d4805-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d4805-118">**Type**</span></span>|<span data-ttu-id="d4805-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4805-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4805-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4805-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4805-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="d4805-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d4805-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="d4805-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d4805-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4805-123">Child elements</span></span>

<span data-ttu-id="d4805-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4805-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4805-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4805-125">Attributes</span></span>

|<span data-ttu-id="d4805-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d4805-126">**Attribute**</span></span>|<span data-ttu-id="d4805-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d4805-127">**Type**</span></span>|<span data-ttu-id="d4805-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d4805-128">**Required**</span></span>|<span data-ttu-id="d4805-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4805-129">**Description**</span></span>|<span data-ttu-id="d4805-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d4805-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d4805-131">PageID</span><span class="sxs-lookup"><span data-stu-id="d4805-131">PageID</span></span>  <br/> |<span data-ttu-id="d4805-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4805-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4805-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d4805-133">required</span></span>  <br/> |<span data-ttu-id="d4805-134">Seiten-ID der Form, die mit Daten in der Datensatzgruppe verknüpft ist, die durch **ROWID**identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d4805-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="d4805-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d4805-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d4805-136">RowID</span><span class="sxs-lookup"><span data-stu-id="d4805-136">RowID</span></span>  <br/> |<span data-ttu-id="d4805-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4805-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4805-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d4805-138">required</span></span>  <br/> |<span data-ttu-id="d4805-139">Zeilen-ID der Zeile, eindeutig innerhalb des Datenrecordsets.</span><span class="sxs-lookup"><span data-stu-id="d4805-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="d4805-140">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d4805-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d4805-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="d4805-141">ShapeID</span></span>  <br/> |<span data-ttu-id="d4805-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4805-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4805-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d4805-143">required</span></span>  <br/> |<span data-ttu-id="d4805-144">Shape-ID der Form, die mit Daten in der Datensatzgruppe verknüpft ist, die durch **ROWID**identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d4805-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="d4805-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="d4805-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

