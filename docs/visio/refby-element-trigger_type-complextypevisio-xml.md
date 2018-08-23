---
title: RefBy-Element (Trigger_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572431"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="32f27-103">RefBy-Element (Trigger_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="32f27-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="32f27-104">Gibt einen Verweis auf eine Seite in der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="32f27-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32f27-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32f27-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32f27-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="32f27-106">**Element type**</span></span> <br/> |[<span data-ttu-id="32f27-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="32f27-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="32f27-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="32f27-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="32f27-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="32f27-109">**Schema file**</span></span> <br/> |<span data-ttu-id="32f27-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="32f27-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="32f27-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="32f27-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="32f27-112">Definition</span><span class="sxs-lookup"><span data-stu-id="32f27-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32f27-113">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="32f27-113">Elements and attributes</span></span>

<span data-ttu-id="32f27-114">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="32f27-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="32f27-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32f27-115">Parent elements</span></span>

|<span data-ttu-id="32f27-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="32f27-116">**Element**</span></span>|<span data-ttu-id="32f27-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="32f27-117">**Type**</span></span>|<span data-ttu-id="32f27-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32f27-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32f27-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="32f27-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="32f27-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="32f27-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32f27-121">Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="32f27-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="32f27-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32f27-122">Child elements</span></span>

<span data-ttu-id="32f27-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="32f27-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32f27-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="32f27-124">Attributes</span></span>

|<span data-ttu-id="32f27-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="32f27-125">**Attribute**</span></span>|<span data-ttu-id="32f27-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="32f27-126">**Type**</span></span>|<span data-ttu-id="32f27-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="32f27-127">**Required**</span></span>|<span data-ttu-id="32f27-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32f27-128">**Description**</span></span>|<span data-ttu-id="32f27-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="32f27-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="32f27-130">ID</span><span class="sxs-lookup"><span data-stu-id="32f27-130">ID</span></span>  <br/> |<span data-ttu-id="32f27-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32f27-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32f27-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="32f27-132">required</span></span>  <br/> |<span data-ttu-id="32f27-133">Gibt das ID-Attribut des einer Seite in der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="32f27-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="32f27-134">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32f27-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32f27-135">T</span><span class="sxs-lookup"><span data-stu-id="32f27-135">T</span></span>  <br/> |<span data-ttu-id="32f27-136">XSD: String</span><span class="sxs-lookup"><span data-stu-id="32f27-136">xsd:string</span></span>  <br/> |<span data-ttu-id="32f27-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="32f27-137">required</span></span>  <br/> |<span data-ttu-id="32f27-138">Gibt den Verweistyp an.</span><span class="sxs-lookup"><span data-stu-id="32f27-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="32f27-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="32f27-139">Values of the xsd:string type.</span></span>  <br/> |
   

