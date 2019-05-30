---
title: RefBy-Element (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung an.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538291"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="58e3d-103">RefBy-Element (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="58e3d-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="58e3d-104">Gibt einen Verweis auf eine Seite in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="58e3d-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58e3d-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="58e3d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58e3d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="58e3d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="58e3d-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="58e3d-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="58e3d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="58e3d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="58e3d-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="58e3d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="58e3d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="58e3d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="58e3d-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="58e3d-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="58e3d-112">Definition</span><span class="sxs-lookup"><span data-stu-id="58e3d-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58e3d-113">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="58e3d-113">Elements and attributes</span></span>

<span data-ttu-id="58e3d-114">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="58e3d-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="58e3d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58e3d-115">Parent elements</span></span>

|<span data-ttu-id="58e3d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="58e3d-116">**Element**</span></span>|<span data-ttu-id="58e3d-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58e3d-117">**Type**</span></span>|<span data-ttu-id="58e3d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58e3d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58e3d-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="58e3d-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="58e3d-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="58e3d-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58e3d-121">Enthält Anweisungen zum Microsoft Visio zum Neuberechnen einer Beziehung zwischen Dokument Parts in einer Visio-Datei.</span><span class="sxs-lookup"><span data-stu-id="58e3d-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="58e3d-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58e3d-122">Child elements</span></span>

<span data-ttu-id="58e3d-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="58e3d-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58e3d-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="58e3d-124">Attributes</span></span>

|<span data-ttu-id="58e3d-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="58e3d-125">**Attribute**</span></span>|<span data-ttu-id="58e3d-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58e3d-126">**Type**</span></span>|<span data-ttu-id="58e3d-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="58e3d-127">**Required**</span></span>|<span data-ttu-id="58e3d-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58e3d-128">**Description**</span></span>|<span data-ttu-id="58e3d-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="58e3d-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58e3d-130">ID</span><span class="sxs-lookup"><span data-stu-id="58e3d-130">ID</span></span>  <br/> |<span data-ttu-id="58e3d-131">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58e3d-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58e3d-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58e3d-132">required</span></span>  <br/> |<span data-ttu-id="58e3d-133">Gibt das ID-Attribut eines Zeichenblatts in der Zeichnung an.</span><span class="sxs-lookup"><span data-stu-id="58e3d-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="58e3d-134">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="58e3d-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58e3d-135">T</span><span class="sxs-lookup"><span data-stu-id="58e3d-135">T</span></span>  <br/> |<span data-ttu-id="58e3d-136">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="58e3d-136">xsd:string</span></span>  <br/> |<span data-ttu-id="58e3d-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58e3d-137">required</span></span>  <br/> |<span data-ttu-id="58e3d-138">Gibt den Verweistyp an.</span><span class="sxs-lookup"><span data-stu-id="58e3d-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="58e3d-139">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="58e3d-139">Values of the xsd:string type.</span></span>  <br/> |
   

