---
title: RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Daten-Recordsets in Konflikt steht.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542835"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="47f41-103">RefreshConflict-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="47f41-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="47f41-104">Gibt eine Zeile im Datenrecordset an, die mit einem Shape verknüpft ist, das nach dem Aktualisieren des Daten-Recordsets in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="47f41-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47f41-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="47f41-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47f41-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="47f41-106">**Element type**</span></span> <br/> |[<span data-ttu-id="47f41-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="47f41-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="47f41-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47f41-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="47f41-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="47f41-109">**Schema file**</span></span> <br/> |<span data-ttu-id="47f41-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="47f41-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="47f41-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="47f41-111">**Document parts**</span></span> <br/> |<span data-ttu-id="47f41-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="47f41-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47f41-113">Definition</span><span class="sxs-lookup"><span data-stu-id="47f41-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47f41-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="47f41-114">Elements and attributes</span></span>

<span data-ttu-id="47f41-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="47f41-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="47f41-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47f41-116">Parent elements</span></span>

|<span data-ttu-id="47f41-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="47f41-117">**Element**</span></span>|<span data-ttu-id="47f41-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="47f41-118">**Type**</span></span>|<span data-ttu-id="47f41-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47f41-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47f41-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="47f41-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="47f41-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="47f41-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47f41-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="47f41-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="47f41-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47f41-123">Child elements</span></span>

<span data-ttu-id="47f41-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="47f41-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47f41-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="47f41-125">Attributes</span></span>

|<span data-ttu-id="47f41-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47f41-126">**Attribute**</span></span>|<span data-ttu-id="47f41-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="47f41-127">**Type**</span></span>|<span data-ttu-id="47f41-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="47f41-128">**Required**</span></span>|<span data-ttu-id="47f41-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47f41-129">**Description**</span></span>|<span data-ttu-id="47f41-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="47f41-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47f41-131">PageID</span><span class="sxs-lookup"><span data-stu-id="47f41-131">PageID</span></span>  <br/> |<span data-ttu-id="47f41-132">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47f41-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47f41-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f41-133">required</span></span>  <br/> |<span data-ttu-id="47f41-134">Seiten-ID der Form, die an dem Konflikt beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="47f41-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="47f41-135">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47f41-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="47f41-136">ROWID</span><span class="sxs-lookup"><span data-stu-id="47f41-136">RowID</span></span>  <br/> |<span data-ttu-id="47f41-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47f41-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47f41-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f41-138">required</span></span>  <br/> |<span data-ttu-id="47f41-139">Die ursprüngliche Zeilen-ID der Zeile, die nach dem Aktualisieren der Daten jetzt in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="47f41-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="47f41-140">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47f41-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="47f41-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="47f41-141">ShapeID</span></span>  <br/> |<span data-ttu-id="47f41-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="47f41-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="47f41-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f41-143">required</span></span>  <br/> |<span data-ttu-id="47f41-144">Shape-ID der Form, die an dem Konflikt beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="47f41-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="47f41-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="47f41-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

