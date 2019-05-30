---
title: Connect-Element (Connects_Type complexType) (Visio XML)
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
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="1ed3e-103">Connect-Element (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1ed3e-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1ed3e-104">Repräsentiert eine Verbindung zwischen zwei Shapes in einer Zeichnung, wie z. B. eine Linie und ein Feld in einem Organigramm.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ed3e-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1ed3e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ed3e-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1ed3e-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="1ed3e-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ed3e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ed3e-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1ed3e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1ed3e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ed3e-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1ed3e-112">Seite #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="1ed3e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ed3e-113">Definition</span><span class="sxs-lookup"><span data-stu-id="1ed3e-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ed3e-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1ed3e-114">Elements and attributes</span></span>

<span data-ttu-id="1ed3e-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ed3e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ed3e-116">Parent elements</span></span>

|<span data-ttu-id="1ed3e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-117">**Element**</span></span>|<span data-ttu-id="1ed3e-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-118">**Type**</span></span>|<span data-ttu-id="1ed3e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ed3e-120">Connects</span><span class="sxs-lookup"><span data-stu-id="1ed3e-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ed3e-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="1ed3e-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ed3e-122">Enthält ein **Connect** -Element für jede Verbindung zwischen zwei Formen in einer Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ed3e-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ed3e-123">Child elements</span></span>

<span data-ttu-id="1ed3e-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ed3e-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ed3e-125">Attributes</span></span>

|<span data-ttu-id="1ed3e-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-126">**Attribute**</span></span>|<span data-ttu-id="1ed3e-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-127">**Type**</span></span>|<span data-ttu-id="1ed3e-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-128">**Required**</span></span>|<span data-ttu-id="1ed3e-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-129">**Description**</span></span>|<span data-ttu-id="1ed3e-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1ed3e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ed3e-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="1ed3e-131">FromCell</span></span>  <br/> |<span data-ttu-id="1ed3e-132">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ed3e-132">xsd:string</span></span>  <br/> |<span data-ttu-id="1ed3e-133">Optional</span><span class="sxs-lookup"><span data-stu-id="1ed3e-133">optional</span></span>  <br/> |<span data-ttu-id="1ed3e-134">Die Zelle, aus der eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="1ed3e-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ed3e-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="1ed3e-136">FromPart</span></span>  <br/> |<span data-ttu-id="1ed3e-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1ed3e-137">xsd:int</span></span>  <br/> |<span data-ttu-id="1ed3e-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1ed3e-138">optional</span></span>  <br/> |<span data-ttu-id="1ed3e-139">Der Teil eines Shapes, von dem eine Verbindung stammt.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="1ed3e-140">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1ed3e-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="1ed3e-141">FromSheet</span></span>  <br/> |<span data-ttu-id="1ed3e-142">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ed3e-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ed3e-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1ed3e-143">required</span></span>  <br/> |<span data-ttu-id="1ed3e-144">Die ID der Form, aus der eine Verbindung oder Verbindungen stammen.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="1ed3e-145">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ed3e-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="1ed3e-146">ToCell</span></span>  <br/> |<span data-ttu-id="1ed3e-147">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ed3e-147">xsd:string</span></span>  <br/> |<span data-ttu-id="1ed3e-148">Optional</span><span class="sxs-lookup"><span data-stu-id="1ed3e-148">optional</span></span>  <br/> |<span data-ttu-id="1ed3e-149">Die Zelle, in der eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="1ed3e-150">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ed3e-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="1ed3e-151">ToPart</span></span>  <br/> |<span data-ttu-id="1ed3e-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1ed3e-152">xsd:int</span></span>  <br/> |<span data-ttu-id="1ed3e-153">Optional</span><span class="sxs-lookup"><span data-stu-id="1ed3e-153">optional</span></span>  <br/> |<span data-ttu-id="1ed3e-154">Der Teil eines Shapes, mit dem eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="1ed3e-155">Werte des Typs XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="1ed3e-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="1ed3e-156">ToSheet</span></span>  <br/> |<span data-ttu-id="1ed3e-157">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ed3e-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ed3e-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1ed3e-158">required</span></span>  <br/> |<span data-ttu-id="1ed3e-159">Die ID der Form, in die mindestens eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="1ed3e-160">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1ed3e-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

