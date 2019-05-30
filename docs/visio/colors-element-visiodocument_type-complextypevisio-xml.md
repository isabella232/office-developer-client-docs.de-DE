---
title: Colors-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Enthält die Farbtabelle des Dokuments.
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540175"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="7da84-103">Colors-Element (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7da84-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7da84-104">Enthält die Farbtabelle des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="7da84-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7da84-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7da84-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7da84-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="7da84-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7da84-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="7da84-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7da84-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7da84-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7da84-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="7da84-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7da84-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7da84-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7da84-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="7da84-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7da84-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="7da84-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7da84-113">Definition</span><span class="sxs-lookup"><span data-stu-id="7da84-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7da84-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="7da84-114">Elements and attributes</span></span>

<span data-ttu-id="7da84-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="7da84-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7da84-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7da84-116">Parent elements</span></span>

|<span data-ttu-id="7da84-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7da84-117">**Element**</span></span>|<span data-ttu-id="7da84-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7da84-118">**Type**</span></span>|<span data-ttu-id="7da84-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7da84-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7da84-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7da84-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7da84-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7da84-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7da84-122">Das Stammelement eines Microsoft Visio Dokuments.</span><span class="sxs-lookup"><span data-stu-id="7da84-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7da84-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7da84-123">Child elements</span></span>

|<span data-ttu-id="7da84-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7da84-124">**Element**</span></span>|<span data-ttu-id="7da84-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="7da84-125">**Type**</span></span>|<span data-ttu-id="7da84-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7da84-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7da84-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="7da84-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7da84-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="7da84-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7da84-129">Enthält einen Farbtabellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="7da84-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7da84-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="7da84-130">Attributes</span></span>

<span data-ttu-id="7da84-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="7da84-131">None.</span></span>
  

