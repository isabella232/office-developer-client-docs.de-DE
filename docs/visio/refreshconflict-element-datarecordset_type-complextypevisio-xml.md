---
title: RefreshConflict-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Gibt eine Zeile im Datenrecordset verknüpft ein Shape, das nach der Datenrecordsets ein Konflikt vorliegt.
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797793"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="f888c-103">RefreshConflict-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f888c-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f888c-104">Gibt eine Zeile im Datenrecordset verknüpft ein Shape, das nach der Datenrecordsets ein Konflikt vorliegt.</span><span class="sxs-lookup"><span data-stu-id="f888c-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f888c-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f888c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f888c-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f888c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f888c-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="f888c-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f888c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f888c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f888c-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f888c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f888c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f888c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f888c-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="f888c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f888c-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="f888c-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f888c-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f888c-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f888c-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f888c-114">Elements and attributes</span></span>

<span data-ttu-id="f888c-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f888c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f888c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f888c-116">Parent elements</span></span>

|<span data-ttu-id="f888c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f888c-117">**Element**</span></span>|<span data-ttu-id="f888c-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f888c-118">**Type**</span></span>|<span data-ttu-id="f888c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f888c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f888c-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="f888c-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f888c-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="f888c-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f888c-122">Speichert, formatiert und aktualisiert Daten, die aus einer Datenbank in Microsoft Visio abgefragt wurden, und zeigt diese Daten an.</span><span class="sxs-lookup"><span data-stu-id="f888c-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f888c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f888c-123">Child elements</span></span>

<span data-ttu-id="f888c-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="f888c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f888c-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="f888c-125">Attributes</span></span>

|<span data-ttu-id="f888c-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f888c-126">**Attribute**</span></span>|<span data-ttu-id="f888c-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f888c-127">**Type**</span></span>|<span data-ttu-id="f888c-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f888c-128">**Required**</span></span>|<span data-ttu-id="f888c-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f888c-129">**Description**</span></span>|<span data-ttu-id="f888c-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f888c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f888c-131">PageID</span><span class="sxs-lookup"><span data-stu-id="f888c-131">PageID</span></span>  <br/> |<span data-ttu-id="f888c-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f888c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f888c-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f888c-133">required</span></span>  <br/> |<span data-ttu-id="f888c-134">Seiten-ID der Form, die den Konflikt beteiligt.</span><span class="sxs-lookup"><span data-stu-id="f888c-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="f888c-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f888c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f888c-136">RowID</span><span class="sxs-lookup"><span data-stu-id="f888c-136">RowID</span></span>  <br/> |<span data-ttu-id="f888c-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f888c-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f888c-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f888c-138">required</span></span>  <br/> |<span data-ttu-id="f888c-139">Die ursprünglichen Zeilen-ID der Zeile jetzt in Konflikt nachdem Daten aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f888c-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="f888c-140">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f888c-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f888c-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="f888c-141">ShapeID</span></span>  <br/> |<span data-ttu-id="f888c-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f888c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f888c-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f888c-143">required</span></span>  <br/> |<span data-ttu-id="f888c-144">Shape-ID der Form, die den Konflikt beteiligt.</span><span class="sxs-lookup"><span data-stu-id="f888c-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="f888c-145">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f888c-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

