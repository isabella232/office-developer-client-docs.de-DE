---
title: AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte in der übergeordneten DataRecordset-Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796423"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="7cc72-103">AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="7cc72-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7cc72-104">Definiert eine Regel, die eine Spalte in der übergeordneten **DataRecordset** -Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.</span><span class="sxs-lookup"><span data-stu-id="7cc72-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7cc72-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7cc72-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cc72-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7cc72-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7cc72-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="7cc72-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7cc72-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7cc72-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7cc72-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7cc72-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7cc72-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7cc72-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7cc72-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="7cc72-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7cc72-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="7cc72-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cc72-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7cc72-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7cc72-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7cc72-114">Elements and attributes</span></span>

<span data-ttu-id="7cc72-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7cc72-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7cc72-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cc72-116">Parent elements</span></span>

|<span data-ttu-id="7cc72-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cc72-117">**Element**</span></span>|<span data-ttu-id="7cc72-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7cc72-118">**Type**</span></span>|<span data-ttu-id="7cc72-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cc72-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7cc72-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="7cc72-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7cc72-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7cc72-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cc72-122">Gibt ein Recordset-Objekt und die Datenbindung zwischen, Recordset und Shapes in Zeichnungseinheiten Seiten.</span><span class="sxs-lookup"><span data-stu-id="7cc72-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7cc72-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cc72-123">Child elements</span></span>

<span data-ttu-id="7cc72-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cc72-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cc72-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="7cc72-125">Attributes</span></span>

|<span data-ttu-id="7cc72-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7cc72-126">**Attribute**</span></span>|<span data-ttu-id="7cc72-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7cc72-127">**Type**</span></span>|<span data-ttu-id="7cc72-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="7cc72-128">**Required**</span></span>|<span data-ttu-id="7cc72-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cc72-129">**Description**</span></span>|<span data-ttu-id="7cc72-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="7cc72-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7cc72-131">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="7cc72-131">ColumnName</span></span>  <br/> |<span data-ttu-id="7cc72-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7cc72-132">xsd:string</span></span>  <br/> |<span data-ttu-id="7cc72-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7cc72-133">required</span></span>  <br/> |<span data-ttu-id="7cc72-134">Ein Spaltenname in das ADO-Recordset-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="7cc72-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="7cc72-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7cc72-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cc72-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="7cc72-136">ContextType</span></span>  <br/> |<span data-ttu-id="7cc72-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7cc72-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7cc72-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="7cc72-138">required</span></span>  <br/> |<span data-ttu-id="7cc72-139">Gibt die Eigenschaften der Gruppe oder ein Shape, die für den Vergleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cc72-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="7cc72-140">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cc72-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="7cc72-141">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7cc72-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7cc72-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="7cc72-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="7cc72-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="7cc72-143">xsd:string</span></span>  <br/> |<span data-ttu-id="7cc72-144">Optional</span><span class="sxs-lookup"><span data-stu-id="7cc72-144">optional</span></span>  <br/> |<span data-ttu-id="7cc72-145">Ist der Wert ContextType 2 oder 3, ist dieses Attribut erforderlich, um einen Vergleich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7cc72-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="7cc72-146">ContextType = 2, ContextTypeLabel muss, werden die Form Element Beschriftung, und wenn **ContextType** = 3, ContextTypeLabel muss der lokale Zeilenname.</span><span class="sxs-lookup"><span data-stu-id="7cc72-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="7cc72-147">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7cc72-147">Values of the xsd:string type.</span></span>  <br/> |
   

