---
title: RefBy-Element (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538291"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="68da8-103">RefBy-Element (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="68da8-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="68da8-104">Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="68da8-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68da8-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68da8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68da8-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="68da8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68da8-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="68da8-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68da8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68da8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68da8-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="68da8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68da8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="68da8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68da8-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="68da8-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="68da8-112">Definition</span><span class="sxs-lookup"><span data-stu-id="68da8-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68da8-113">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="68da8-113">Elements and attributes</span></span>

<span data-ttu-id="68da8-114">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="68da8-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68da8-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68da8-115">Parent elements</span></span>

|<span data-ttu-id="68da8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="68da8-116">**Element**</span></span>|<span data-ttu-id="68da8-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68da8-117">**Type**</span></span>|<span data-ttu-id="68da8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68da8-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68da8-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="68da8-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="68da8-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="68da8-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68da8-121">Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokumentteilen in einer Visio zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="68da8-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="68da8-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68da8-122">Child elements</span></span>

<span data-ttu-id="68da8-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="68da8-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68da8-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="68da8-124">Attributes</span></span>

|<span data-ttu-id="68da8-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68da8-125">**Attribute**</span></span>|<span data-ttu-id="68da8-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="68da8-126">**Type**</span></span>|<span data-ttu-id="68da8-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="68da8-127">**Required**</span></span>|<span data-ttu-id="68da8-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68da8-128">**Description**</span></span>|<span data-ttu-id="68da8-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="68da8-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68da8-130">ID</span><span class="sxs-lookup"><span data-stu-id="68da8-130">ID</span></span>  <br/> |<span data-ttu-id="68da8-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68da8-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68da8-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="68da8-132">required</span></span>  <br/> |<span data-ttu-id="68da8-133">Gibt das ID-Attribut einer Seite in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="68da8-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="68da8-134">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="68da8-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68da8-135">T</span><span class="sxs-lookup"><span data-stu-id="68da8-135">T</span></span>  <br/> |<span data-ttu-id="68da8-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="68da8-136">xsd:string</span></span>  <br/> |<span data-ttu-id="68da8-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="68da8-137">required</span></span>  <br/> |<span data-ttu-id="68da8-138">Gibt den Referenztyp an.</span><span class="sxs-lookup"><span data-stu-id="68da8-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="68da8-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="68da8-139">Values of the xsd:string type.</span></span>  <br/> |
   

