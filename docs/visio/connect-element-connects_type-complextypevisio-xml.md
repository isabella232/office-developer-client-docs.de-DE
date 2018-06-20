---
title: Verbinden-Element (Connects_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Stellt eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie etwa eine Linie und ein Feld in einem Organigramm dar.
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796713"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="9fc62-103">Verbinden-Element (Connects_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="9fc62-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9fc62-104">Stellt eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie etwa eine Linie und ein Feld in einem Organigramm dar.</span><span class="sxs-lookup"><span data-stu-id="9fc62-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fc62-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9fc62-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fc62-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9fc62-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fc62-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="9fc62-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fc62-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9fc62-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fc62-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9fc62-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fc62-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9fc62-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fc62-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="9fc62-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fc62-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="9fc62-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fc62-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9fc62-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fc62-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9fc62-114">Elements and attributes</span></span>

<span data-ttu-id="9fc62-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="9fc62-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fc62-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fc62-116">Parent elements</span></span>

|<span data-ttu-id="9fc62-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fc62-117">**Element**</span></span>|<span data-ttu-id="9fc62-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9fc62-118">**Type**</span></span>|<span data-ttu-id="9fc62-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fc62-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fc62-120">Stellt eine Verbindung her</span><span class="sxs-lookup"><span data-stu-id="9fc62-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc62-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="9fc62-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fc62-122">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Shapes in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="9fc62-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fc62-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fc62-123">Child elements</span></span>

<span data-ttu-id="9fc62-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fc62-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fc62-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fc62-125">Attributes</span></span>

|<span data-ttu-id="9fc62-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9fc62-126">**Attribute**</span></span>|<span data-ttu-id="9fc62-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9fc62-127">**Type**</span></span>|<span data-ttu-id="9fc62-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9fc62-128">**Required**</span></span>|<span data-ttu-id="9fc62-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fc62-129">**Description**</span></span>|<span data-ttu-id="9fc62-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9fc62-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fc62-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="9fc62-131">FromCell</span></span>  <br/> |<span data-ttu-id="9fc62-132">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9fc62-132">xsd:string</span></span>  <br/> |<span data-ttu-id="9fc62-133">Optional</span><span class="sxs-lookup"><span data-stu-id="9fc62-133">optional</span></span>  <br/> |<span data-ttu-id="9fc62-134">Die Zelle, von der eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="9fc62-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="9fc62-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9fc62-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9fc62-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="9fc62-136">FromPart</span></span>  <br/> |<span data-ttu-id="9fc62-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="9fc62-137">xsd:int</span></span>  <br/> |<span data-ttu-id="9fc62-138">Optional</span><span class="sxs-lookup"><span data-stu-id="9fc62-138">optional</span></span>  <br/> |<span data-ttu-id="9fc62-139">Der Teil eines Shapes, von dem eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="9fc62-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="9fc62-140">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="9fc62-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="9fc62-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="9fc62-141">FromSheet</span></span>  <br/> |<span data-ttu-id="9fc62-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9fc62-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9fc62-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9fc62-143">required</span></span>  <br/> |<span data-ttu-id="9fc62-144">Die ID des Shapes, aus denen eine Verbindung oder Verbindungen stammen.</span><span class="sxs-lookup"><span data-stu-id="9fc62-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="9fc62-145">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9fc62-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9fc62-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="9fc62-146">ToCell</span></span>  <br/> |<span data-ttu-id="9fc62-147">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9fc62-147">xsd:string</span></span>  <br/> |<span data-ttu-id="9fc62-148">Optional</span><span class="sxs-lookup"><span data-stu-id="9fc62-148">optional</span></span>  <br/> |<span data-ttu-id="9fc62-149">Die Zelle mit der eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9fc62-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="9fc62-150">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9fc62-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9fc62-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="9fc62-151">ToPart</span></span>  <br/> |<span data-ttu-id="9fc62-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="9fc62-152">xsd:int</span></span>  <br/> |<span data-ttu-id="9fc62-153">Optional</span><span class="sxs-lookup"><span data-stu-id="9fc62-153">optional</span></span>  <br/> |<span data-ttu-id="9fc62-154">Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9fc62-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="9fc62-155">Werte des Typs xsd: int.</span><span class="sxs-lookup"><span data-stu-id="9fc62-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="9fc62-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="9fc62-156">ToSheet</span></span>  <br/> |<span data-ttu-id="9fc62-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9fc62-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9fc62-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9fc62-158">required</span></span>  <br/> |<span data-ttu-id="9fc62-159">Die ID des das Shape, mit dem eine oder mehrere Verbindungen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9fc62-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="9fc62-160">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9fc62-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

