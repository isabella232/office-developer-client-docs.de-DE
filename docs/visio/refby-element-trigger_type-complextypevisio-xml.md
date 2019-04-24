---
title: RefBy-Element (Trigger_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung an.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348405"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="cb8b1-103">RefBy-Element (Trigger_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cb8b1-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cb8b1-104">Gibt einen Verweis auf eine Seite in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb8b1-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cb8b1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb8b1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb8b1-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="cb8b1-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb8b1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb8b1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb8b1-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="cb8b1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb8b1-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="cb8b1-112">Definition</span><span class="sxs-lookup"><span data-stu-id="cb8b1-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb8b1-113">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cb8b1-113">Elements and attributes</span></span>

<span data-ttu-id="cb8b1-114">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb8b1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb8b1-115">Parent elements</span></span>

|<span data-ttu-id="cb8b1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-116">**Element**</span></span>|<span data-ttu-id="cb8b1-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-117">**Type**</span></span>|<span data-ttu-id="cb8b1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb8b1-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="cb8b1-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="cb8b1-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="cb8b1-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb8b1-121">Enthält Anweisungen für Microsoft Visio, um eine Beziehung zwischen Dokument Teilen in einer Visio-Datei neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="cb8b1-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb8b1-122">Child elements</span></span>

<span data-ttu-id="cb8b1-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb8b1-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb8b1-124">Attributes</span></span>

|<span data-ttu-id="cb8b1-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-125">**Attribute**</span></span>|<span data-ttu-id="cb8b1-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-126">**Type**</span></span>|<span data-ttu-id="cb8b1-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-127">**Required**</span></span>|<span data-ttu-id="cb8b1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-128">**Description**</span></span>|<span data-ttu-id="cb8b1-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb8b1-130">ID</span><span class="sxs-lookup"><span data-stu-id="cb8b1-130">ID</span></span>  <br/> |<span data-ttu-id="cb8b1-131">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cb8b1-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb8b1-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="cb8b1-132">required</span></span>  <br/> |<span data-ttu-id="cb8b1-133">Gibt das ID-Attribut einer Seite in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="cb8b1-134">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb8b1-135">T</span><span class="sxs-lookup"><span data-stu-id="cb8b1-135">T</span></span>  <br/> |<span data-ttu-id="cb8b1-136">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cb8b1-136">xsd:string</span></span>  <br/> |<span data-ttu-id="cb8b1-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="cb8b1-137">required</span></span>  <br/> |<span data-ttu-id="cb8b1-138">Gibt den Verweistyp an.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="cb8b1-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-139">Values of the xsd:string type.</span></span>  <br/> |
   

