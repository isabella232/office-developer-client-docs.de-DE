---
title: AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537871"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="6cfd8-103">AutoLinkComparison-Element (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6cfd8-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6cfd8-104">Definiert eine Regel, die eine Spalte im übergeordneten DataRecordset-Element mit einem Shape-Datenelement aus der letzten erfolgreichen automatischen Verknüpfungsaktion vergleicht, die auf der Benutzeroberfläche ausgeführt wurde. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6cfd8-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6cfd8-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6cfd8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6cfd8-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6cfd8-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="6cfd8-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6cfd8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6cfd8-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6cfd8-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6cfd8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6cfd8-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6cfd8-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="6cfd8-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6cfd8-113">Definition</span><span class="sxs-lookup"><span data-stu-id="6cfd8-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6cfd8-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6cfd8-114">Elements and attributes</span></span>

<span data-ttu-id="6cfd8-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6cfd8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6cfd8-116">Parent elements</span></span>

|<span data-ttu-id="6cfd8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-117">**Element**</span></span>|<span data-ttu-id="6cfd8-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-118">**Type**</span></span>|<span data-ttu-id="6cfd8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6cfd8-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="6cfd8-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6cfd8-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="6cfd8-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6cfd8-122">Gibt ein Recordset-Objekt und die Datenbindung zwischen dem Recordset-Objekt und Shapes auf Zeichen Seiten an.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6cfd8-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6cfd8-123">Child elements</span></span>

<span data-ttu-id="6cfd8-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6cfd8-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="6cfd8-125">Attributes</span></span>

|<span data-ttu-id="6cfd8-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-126">**Attribute**</span></span>|<span data-ttu-id="6cfd8-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-127">**Type**</span></span>|<span data-ttu-id="6cfd8-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-128">**Required**</span></span>|<span data-ttu-id="6cfd8-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-129">**Description**</span></span>|<span data-ttu-id="6cfd8-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6cfd8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6cfd8-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="6cfd8-131">ColumnName</span></span>  <br/> |<span data-ttu-id="6cfd8-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6cfd8-132">xsd:string</span></span>  <br/> |<span data-ttu-id="6cfd8-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6cfd8-133">required</span></span>  <br/> |<span data-ttu-id="6cfd8-134">Entspricht einem Spaltennamen im ADO-Recordset-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="6cfd8-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6cfd8-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="6cfd8-136">ContextType</span></span>  <br/> |<span data-ttu-id="6cfd8-137">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6cfd8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6cfd8-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6cfd8-138">required</span></span>  <br/> |<span data-ttu-id="6cfd8-139">Gibt die Eigenschaften der Gruppe oder der Form an, die für den Vergleich verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="6cfd8-140">Mögliche Werte sind in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="6cfd8-141">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6cfd8-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="6cfd8-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="6cfd8-143">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6cfd8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6cfd8-144">Optional</span><span class="sxs-lookup"><span data-stu-id="6cfd8-144">optional</span></span>  <br/> |<span data-ttu-id="6cfd8-145">Wenn der ContextType-Wert 2 oder 3 ist, ist dieses Attribut erforderlich, um einen Vergleich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="6cfd8-146">Bei ContextType = 2 muss ContextTypeLabel die Shape-Datenelement Bezeichnung sein, und wenn **ContextType** = 3 lautet, muss ContextTypeLabel der Name der lokalen Zeile sein.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="6cfd8-147">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6cfd8-147">Values of the xsd:string type.</span></span>  <br/> |
   

