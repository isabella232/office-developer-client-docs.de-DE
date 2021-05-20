---
title: Verbinden -Element (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541995"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="f3a7b-103">Verbinden -Element (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f3a7b-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f3a7b-104">Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3a7b-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f3a7b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3a7b-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f3a7b-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="f3a7b-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f3a7b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f3a7b-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f3a7b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f3a7b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f3a7b-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f3a7b-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="f3a7b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3a7b-113">Definition</span><span class="sxs-lookup"><span data-stu-id="f3a7b-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3a7b-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f3a7b-114">Elements and attributes</span></span>

<span data-ttu-id="f3a7b-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f3a7b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a7b-116">Parent elements</span></span>

|<span data-ttu-id="f3a7b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-117">**Element**</span></span>|<span data-ttu-id="f3a7b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-118">**Type**</span></span>|<span data-ttu-id="f3a7b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3a7b-120">Connects</span><span class="sxs-lookup"><span data-stu-id="f3a7b-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3a7b-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="f3a7b-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f3a7b-122">Enthält ein **Verbinden-Element** für jede Verbindung zwischen zwei Formen in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f3a7b-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3a7b-123">Child elements</span></span>

<span data-ttu-id="f3a7b-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3a7b-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3a7b-125">Attributes</span></span>

|<span data-ttu-id="f3a7b-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-126">**Attribute**</span></span>|<span data-ttu-id="f3a7b-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-127">**Type**</span></span>|<span data-ttu-id="f3a7b-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-128">**Required**</span></span>|<span data-ttu-id="f3a7b-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-129">**Description**</span></span>|<span data-ttu-id="f3a7b-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f3a7b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3a7b-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="f3a7b-131">FromCell</span></span>  <br/> |<span data-ttu-id="f3a7b-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f3a7b-132">xsd:string</span></span>  <br/> |<span data-ttu-id="f3a7b-133">Optional</span><span class="sxs-lookup"><span data-stu-id="f3a7b-133">optional</span></span>  <br/> |<span data-ttu-id="f3a7b-134">Die Zelle, aus der eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="f3a7b-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3a7b-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="f3a7b-136">FromPart</span></span>  <br/> |<span data-ttu-id="f3a7b-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="f3a7b-137">xsd:int</span></span>  <br/> |<span data-ttu-id="f3a7b-138">Optional</span><span class="sxs-lookup"><span data-stu-id="f3a7b-138">optional</span></span>  <br/> |<span data-ttu-id="f3a7b-139">Der Teil eines Shapes, von dem eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="f3a7b-140">Werte des xsd:int-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="f3a7b-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="f3a7b-141">FromSheet</span></span>  <br/> |<span data-ttu-id="f3a7b-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3a7b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3a7b-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f3a7b-143">required</span></span>  <br/> |<span data-ttu-id="f3a7b-144">Die ID des Shapes, von dem eine Verbindung oder Verbindungen stammen.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="f3a7b-145">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3a7b-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="f3a7b-146">ToCell</span></span>  <br/> |<span data-ttu-id="f3a7b-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f3a7b-147">xsd:string</span></span>  <br/> |<span data-ttu-id="f3a7b-148">Optional</span><span class="sxs-lookup"><span data-stu-id="f3a7b-148">optional</span></span>  <br/> |<span data-ttu-id="f3a7b-149">Die Zelle, mit der eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="f3a7b-150">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3a7b-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="f3a7b-151">ToPart</span></span>  <br/> |<span data-ttu-id="f3a7b-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="f3a7b-152">xsd:int</span></span>  <br/> |<span data-ttu-id="f3a7b-153">Optional</span><span class="sxs-lookup"><span data-stu-id="f3a7b-153">optional</span></span>  <br/> |<span data-ttu-id="f3a7b-154">Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="f3a7b-155">Werte des xsd:Int-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="f3a7b-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="f3a7b-156">ToSheet</span></span>  <br/> |<span data-ttu-id="f3a7b-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3a7b-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3a7b-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f3a7b-158">required</span></span>  <br/> |<span data-ttu-id="f3a7b-159">Die ID des Shapes, mit dem eine oder mehrere Verbindungen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="f3a7b-160">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

