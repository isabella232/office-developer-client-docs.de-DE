---
title: Verbinden-Element (Connects_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.\n"
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796713"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="c6f19-103">Verbinden-Element (Connects_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c6f19-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c6f19-104">
			Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
</span><span class="sxs-lookup"><span data-stu-id="c6f19-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6f19-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c6f19-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6f19-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c6f19-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c6f19-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="c6f19-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c6f19-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c6f19-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c6f19-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c6f19-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c6f19-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c6f19-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c6f19-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="c6f19-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c6f19-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="c6f19-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6f19-113">Definition</span><span class="sxs-lookup"><span data-stu-id="c6f19-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6f19-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c6f19-114">Elements and attributes</span></span>

<span data-ttu-id="c6f19-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c6f19-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c6f19-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6f19-116">Parent elements</span></span>

|<span data-ttu-id="c6f19-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c6f19-117">**Element**</span></span>|<span data-ttu-id="c6f19-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c6f19-118">**Type**</span></span>|<span data-ttu-id="c6f19-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6f19-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6f19-120">Connects</span><span class="sxs-lookup"><span data-stu-id="c6f19-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c6f19-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c6f19-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6f19-122">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="c6f19-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6f19-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6f19-123">Child elements</span></span>

<span data-ttu-id="c6f19-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="c6f19-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6f19-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="c6f19-125">Attributes</span></span>

|<span data-ttu-id="c6f19-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c6f19-126">**Attribute**</span></span>|<span data-ttu-id="c6f19-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c6f19-127">**Type**</span></span>|<span data-ttu-id="c6f19-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c6f19-128">**Required**</span></span>|<span data-ttu-id="c6f19-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6f19-129">**Description**</span></span>|<span data-ttu-id="c6f19-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c6f19-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6f19-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="c6f19-131">FromCell</span></span>  <br/> |<span data-ttu-id="c6f19-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c6f19-132">xsd:string</span></span>  <br/> |<span data-ttu-id="c6f19-133">Optional</span><span class="sxs-lookup"><span data-stu-id="c6f19-133">optional</span></span>  <br/> |<span data-ttu-id="c6f19-134">Die Zelle, von der eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="c6f19-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="c6f19-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c6f19-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6f19-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="c6f19-136">FromPart</span></span>  <br/> |<span data-ttu-id="c6f19-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="c6f19-137">xsd:int</span></span>  <br/> |<span data-ttu-id="c6f19-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c6f19-138">optional</span></span>  <br/> |<span data-ttu-id="c6f19-139">Der Teil eines Shapes, von dem eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="c6f19-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="c6f19-140">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="c6f19-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="c6f19-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="c6f19-141">FromSheet</span></span>  <br/> |<span data-ttu-id="c6f19-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c6f19-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c6f19-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6f19-143">required</span></span>  <br/> |<span data-ttu-id="c6f19-144">Die ID des Shapes, aus denen eine Verbindung oder Verbindungen stammen.</span><span class="sxs-lookup"><span data-stu-id="c6f19-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="c6f19-145">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c6f19-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c6f19-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="c6f19-146">ToCell</span></span>  <br/> |<span data-ttu-id="c6f19-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c6f19-147">xsd:string</span></span>  <br/> |<span data-ttu-id="c6f19-148">Optional</span><span class="sxs-lookup"><span data-stu-id="c6f19-148">optional</span></span>  <br/> |<span data-ttu-id="c6f19-149">Die Zelle mit der eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6f19-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="c6f19-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c6f19-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6f19-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="c6f19-151">ToPart</span></span>  <br/> |<span data-ttu-id="c6f19-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="c6f19-152">xsd:int</span></span>  <br/> |<span data-ttu-id="c6f19-153">Optional</span><span class="sxs-lookup"><span data-stu-id="c6f19-153">optional</span></span>  <br/> |<span data-ttu-id="c6f19-154">Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6f19-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="c6f19-155">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="c6f19-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="c6f19-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="c6f19-156">ToSheet</span></span>  <br/> |<span data-ttu-id="c6f19-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c6f19-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c6f19-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6f19-158">required</span></span>  <br/> |<span data-ttu-id="c6f19-159">Die ID des das Shape, mit dem eine oder mehrere Verbindungen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6f19-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="c6f19-160">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c6f19-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

