---
title: Colors-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Tabelle des Dokuments enthält.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400530"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="3f4bc-103">Colors-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3f4bc-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3f4bc-104">Tabelle des Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="3f4bc-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f4bc-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3f4bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f4bc-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3f4bc-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="3f4bc-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3f4bc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3f4bc-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3f4bc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3f4bc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3f4bc-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3f4bc-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="3f4bc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3f4bc-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3f4bc-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3f4bc-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3f4bc-114">Elements and attributes</span></span>

<span data-ttu-id="3f4bc-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3f4bc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3f4bc-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f4bc-116">Parent elements</span></span>

|<span data-ttu-id="3f4bc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-117">**Element**</span></span>|<span data-ttu-id="3f4bc-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-118">**Type**</span></span>|<span data-ttu-id="3f4bc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f4bc-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3f4bc-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3f4bc-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3f4bc-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3f4bc-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="3f4bc-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f4bc-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f4bc-123">Child elements</span></span>

|<span data-ttu-id="3f4bc-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-124">**Element**</span></span>|<span data-ttu-id="3f4bc-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-125">**Type**</span></span>|<span data-ttu-id="3f4bc-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f4bc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f4bc-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="3f4bc-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f4bc-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3f4bc-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3f4bc-129">Enthält einen Eintrag Farbe an.</span><span class="sxs-lookup"><span data-stu-id="3f4bc-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3f4bc-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f4bc-130">Attributes</span></span>

<span data-ttu-id="3f4bc-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f4bc-131">None.</span></span>
  

