---
title: Colors-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Tabelle des Dokuments enthält.
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796652"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="18fce-103">Colors-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="18fce-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="18fce-104">Tabelle des Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="18fce-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18fce-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="18fce-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18fce-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="18fce-106">**Element type**</span></span> <br/> |[<span data-ttu-id="18fce-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="18fce-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="18fce-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="18fce-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="18fce-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="18fce-109">**Schema file**</span></span> <br/> |<span data-ttu-id="18fce-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="18fce-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="18fce-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="18fce-111">**Document parts**</span></span> <br/> |<span data-ttu-id="18fce-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="18fce-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18fce-113">Definition</span><span class="sxs-lookup"><span data-stu-id="18fce-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18fce-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="18fce-114">Elements and attributes</span></span>

<span data-ttu-id="18fce-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="18fce-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="18fce-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18fce-116">Parent elements</span></span>

|<span data-ttu-id="18fce-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="18fce-117">**Element**</span></span>|<span data-ttu-id="18fce-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="18fce-118">**Type**</span></span>|<span data-ttu-id="18fce-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fce-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18fce-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="18fce-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="18fce-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="18fce-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18fce-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="18fce-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18fce-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18fce-123">Child elements</span></span>

|<span data-ttu-id="18fce-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="18fce-124">**Element**</span></span>|<span data-ttu-id="18fce-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="18fce-125">**Type**</span></span>|<span data-ttu-id="18fce-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18fce-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18fce-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="18fce-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18fce-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="18fce-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18fce-129">Enthält einen Eintrag Farbe an.</span><span class="sxs-lookup"><span data-stu-id="18fce-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="18fce-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="18fce-130">Attributes</span></span>

<span data-ttu-id="18fce-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="18fce-131">None.</span></span>
  

