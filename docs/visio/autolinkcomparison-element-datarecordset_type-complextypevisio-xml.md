---
title: AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte in der übergeordneten DataRecordset-Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385718"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="303fe-103">AutoLinkComparison-Element (DataRecordSet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="303fe-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="303fe-104">Definiert eine Regel, die eine Spalte in der übergeordneten **DataRecordset** -Element mit eines Shape-Datenelements aus der letzten erfolgreichen automatische Verknüpfen Aktion auf der Benutzeroberfläche vergleicht.</span><span class="sxs-lookup"><span data-stu-id="303fe-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="303fe-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="303fe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="303fe-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="303fe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="303fe-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="303fe-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="303fe-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="303fe-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="303fe-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="303fe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="303fe-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="303fe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="303fe-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="303fe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="303fe-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="303fe-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="303fe-113">Definition</span><span class="sxs-lookup"><span data-stu-id="303fe-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="303fe-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="303fe-114">Elements and attributes</span></span>

<span data-ttu-id="303fe-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="303fe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="303fe-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="303fe-116">Parent elements</span></span>

|<span data-ttu-id="303fe-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="303fe-117">**Element**</span></span>|<span data-ttu-id="303fe-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="303fe-118">**Type**</span></span>|<span data-ttu-id="303fe-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="303fe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="303fe-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="303fe-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="303fe-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="303fe-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="303fe-122">Gibt ein Recordset-Objekt und die Datenbindung zwischen, Recordset und Shapes in Zeichnungseinheiten Seiten.</span><span class="sxs-lookup"><span data-stu-id="303fe-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="303fe-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="303fe-123">Child elements</span></span>

<span data-ttu-id="303fe-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="303fe-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="303fe-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="303fe-125">Attributes</span></span>

|<span data-ttu-id="303fe-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="303fe-126">**Attribute**</span></span>|<span data-ttu-id="303fe-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="303fe-127">**Type**</span></span>|<span data-ttu-id="303fe-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="303fe-128">**Required**</span></span>|<span data-ttu-id="303fe-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="303fe-129">**Description**</span></span>|<span data-ttu-id="303fe-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="303fe-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="303fe-131">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="303fe-131">ColumnName</span></span>  <br/> |<span data-ttu-id="303fe-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="303fe-132">xsd:string</span></span>  <br/> |<span data-ttu-id="303fe-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="303fe-133">required</span></span>  <br/> |<span data-ttu-id="303fe-134">Ein Spaltenname in das ADO-Recordset-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="303fe-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="303fe-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="303fe-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="303fe-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="303fe-136">ContextType</span></span>  <br/> |<span data-ttu-id="303fe-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="303fe-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="303fe-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="303fe-138">required</span></span>  <br/> |<span data-ttu-id="303fe-139">Gibt die Eigenschaften der Gruppe oder ein Shape, die für den Vergleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="303fe-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="303fe-140">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="303fe-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="303fe-141">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="303fe-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="303fe-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="303fe-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="303fe-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="303fe-143">xsd:string</span></span>  <br/> |<span data-ttu-id="303fe-144">Optional</span><span class="sxs-lookup"><span data-stu-id="303fe-144">optional</span></span>  <br/> |<span data-ttu-id="303fe-145">Ist der Wert ContextType 2 oder 3, ist dieses Attribut erforderlich, um einen Vergleich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="303fe-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="303fe-146">ContextType = 2, ContextTypeLabel muss, werden die Form Element Beschriftung, und wenn **ContextType** = 3, ContextTypeLabel muss der lokale Zeilenname.</span><span class="sxs-lookup"><span data-stu-id="303fe-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="303fe-147">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="303fe-147">Values of the xsd:string type.</span></span>  <br/> |
   

