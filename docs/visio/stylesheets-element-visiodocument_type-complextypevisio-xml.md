---
title: StyleSheets-Element (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Enthält eine Auflistung von StyleSheet-Elementen für das Dokument.
ms.openlocfilehash: 4aae3bcbecec34d961f2d14fd6d3865e7cd332f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329785"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="96949-103">StyleSheets-Element (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="96949-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="96949-104">Enthält eine Auflistung von StyleSheet-Elementen für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="96949-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96949-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="96949-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96949-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="96949-106">**Element type**</span></span> <br/> |[<span data-ttu-id="96949-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="96949-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="96949-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="96949-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="96949-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="96949-109">**Schema file**</span></span> <br/> |<span data-ttu-id="96949-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="96949-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="96949-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="96949-111">**Document parts**</span></span> <br/> |<span data-ttu-id="96949-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="96949-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96949-113">Definition</span><span class="sxs-lookup"><span data-stu-id="96949-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="96949-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="96949-114">Elements and attributes</span></span>

<span data-ttu-id="96949-115">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="96949-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="96949-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96949-116">Parent elements</span></span>

|<span data-ttu-id="96949-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="96949-117">**Element**</span></span>|<span data-ttu-id="96949-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="96949-118">**Type**</span></span>|<span data-ttu-id="96949-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96949-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96949-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="96949-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="96949-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="96949-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96949-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="96949-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="96949-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96949-123">Child elements</span></span>

|<span data-ttu-id="96949-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="96949-124">**Element**</span></span>|<span data-ttu-id="96949-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="96949-125">**Type**</span></span>|<span data-ttu-id="96949-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96949-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96949-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="96949-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96949-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="96949-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96949-129">Repräsentiert eine in einem Dokument definierte Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="96949-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="96949-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="96949-130">Attributes</span></span>

<span data-ttu-id="96949-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="96949-131">None.</span></span>
  

