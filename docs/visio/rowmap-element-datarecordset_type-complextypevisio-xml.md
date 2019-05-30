---
title: RowMap-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Ordnet einer Form eine Data-Recordset-Zeile zu.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540770"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="db98b-103">RowMap-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="db98b-103">RowMap element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="db98b-104">Ordnet einer Form eine Data-Recordset-Zeile zu.</span><span class="sxs-lookup"><span data-stu-id="db98b-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db98b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="db98b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db98b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="db98b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="db98b-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="db98b-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="db98b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db98b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="db98b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="db98b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="db98b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="db98b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="db98b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="db98b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="db98b-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="db98b-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db98b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="db98b-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="db98b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="db98b-114">Elements and attributes</span></span>

<span data-ttu-id="db98b-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="db98b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="db98b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db98b-116">Parent elements</span></span>

****

|<span data-ttu-id="db98b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="db98b-117">**Element**</span></span>|<span data-ttu-id="db98b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="db98b-118">**Type**</span></span>|<span data-ttu-id="db98b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db98b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db98b-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="db98b-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="db98b-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="db98b-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="db98b-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="db98b-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="db98b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db98b-123">Child elements</span></span>

<span data-ttu-id="db98b-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="db98b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db98b-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="db98b-125">Attributes</span></span>

|<span data-ttu-id="db98b-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="db98b-126">**Attribute**</span></span>|<span data-ttu-id="db98b-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="db98b-127">**Type**</span></span>|<span data-ttu-id="db98b-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="db98b-128">**Required**</span></span>|<span data-ttu-id="db98b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db98b-129">**Description**</span></span>|<span data-ttu-id="db98b-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="db98b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db98b-131">PageID</span><span class="sxs-lookup"><span data-stu-id="db98b-131">PageID</span></span>  <br/> |<span data-ttu-id="db98b-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="db98b-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db98b-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="db98b-133">required</span></span>  <br/> |<span data-ttu-id="db98b-134">Seiten-ID des Shapes, das mit Daten in der von **ROWID**identifizierten Datensatzzeile verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="db98b-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="db98b-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="db98b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="db98b-136">ROWID</span><span class="sxs-lookup"><span data-stu-id="db98b-136">RowID</span></span>  <br/> |<span data-ttu-id="db98b-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="db98b-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db98b-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="db98b-138">required</span></span>  <br/> |<span data-ttu-id="db98b-139">Zeilen-ID der Zeile, eindeutig innerhalb des Datenrecordset.</span><span class="sxs-lookup"><span data-stu-id="db98b-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="db98b-140">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="db98b-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="db98b-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="db98b-141">ShapeID</span></span>  <br/> |<span data-ttu-id="db98b-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="db98b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="db98b-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="db98b-143">required</span></span>  <br/> |<span data-ttu-id="db98b-144">Shape-ID des Shapes, das mit Daten in der von **ROWID**identifizierten Datensatzzeile verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="db98b-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="db98b-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="db98b-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

