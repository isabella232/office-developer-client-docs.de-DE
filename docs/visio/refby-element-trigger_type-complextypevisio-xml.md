---
title: RefBy-Element (Trigger_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Gibt einen Verweis auf eine Seite in der Zeichnung.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797783"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="f6919-103">RefBy-Element (Trigger_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="f6919-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f6919-104">Gibt einen Verweis auf eine Seite in der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="f6919-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6919-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f6919-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6919-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f6919-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f6919-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="f6919-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6919-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f6919-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6919-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f6919-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f6919-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f6919-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6919-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="f6919-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="f6919-112">Definition</span><span class="sxs-lookup"><span data-stu-id="f6919-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6919-113">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f6919-113">Elements and attributes</span></span>

<span data-ttu-id="f6919-114">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="f6919-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6919-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6919-115">Parent elements</span></span>

|<span data-ttu-id="f6919-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6919-116">**Element**</span></span>|<span data-ttu-id="f6919-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f6919-117">**Type**</span></span>|<span data-ttu-id="f6919-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6919-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6919-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="f6919-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f6919-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="f6919-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6919-121">Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="f6919-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="f6919-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="f6919-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f6919-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="f6919-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6919-124">Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="f6919-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="f6919-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="f6919-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="f6919-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="f6919-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6919-127">Ermöglicht den Anweisungen auf Microsoft Visio eine Beziehung zwischen Dokumentteile in einer Visio-Datei neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="f6919-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6919-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6919-128">Child elements</span></span>

<span data-ttu-id="f6919-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6919-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6919-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6919-130">Attributes</span></span>

|<span data-ttu-id="f6919-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f6919-131">**Attribute**</span></span>|<span data-ttu-id="f6919-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f6919-132">**Type**</span></span>|<span data-ttu-id="f6919-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6919-133">**Required**</span></span>|<span data-ttu-id="f6919-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6919-134">**Description**</span></span>|<span data-ttu-id="f6919-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f6919-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6919-136">ID</span><span class="sxs-lookup"><span data-stu-id="f6919-136">ID</span></span>  <br/> |<span data-ttu-id="f6919-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f6919-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f6919-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f6919-138">required</span></span>  <br/> |<span data-ttu-id="f6919-139">Gibt das ID-Attribut des einer Seite in der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="f6919-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="f6919-140">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f6919-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f6919-141">T</span><span class="sxs-lookup"><span data-stu-id="f6919-141">T</span></span>  <br/> |<span data-ttu-id="f6919-142">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f6919-142">xsd:string</span></span>  <br/> |<span data-ttu-id="f6919-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f6919-143">required</span></span>  <br/> |<span data-ttu-id="f6919-144">Gibt den Verweistyp an.</span><span class="sxs-lookup"><span data-stu-id="f6919-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="f6919-145">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f6919-145">Values of the xsd:string type.</span></span>  <br/> |
   

