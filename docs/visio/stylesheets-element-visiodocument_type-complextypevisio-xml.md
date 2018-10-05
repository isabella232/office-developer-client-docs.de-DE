---
title: StyleSheets-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Enthält eine Auflistung von StyleSheet-Elemente für das Dokument an.
ms.openlocfilehash: 4aae3bcbecec34d961f2d14fd6d3865e7cd332f6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395826"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="93acb-103">StyleSheets-Element (VisioDocument_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="93acb-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="93acb-104">Enthält eine Auflistung von StyleSheet-Elemente für das Dokument an.</span><span class="sxs-lookup"><span data-stu-id="93acb-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93acb-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="93acb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93acb-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="93acb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="93acb-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="93acb-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="93acb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="93acb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="93acb-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="93acb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="93acb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="93acb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="93acb-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="93acb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="93acb-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="93acb-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93acb-113">Definition</span><span class="sxs-lookup"><span data-stu-id="93acb-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93acb-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="93acb-114">Elements and attributes</span></span>

<span data-ttu-id="93acb-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="93acb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="93acb-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93acb-116">Parent elements</span></span>

|<span data-ttu-id="93acb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="93acb-117">**Element**</span></span>|<span data-ttu-id="93acb-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="93acb-118">**Type**</span></span>|<span data-ttu-id="93acb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93acb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93acb-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="93acb-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="93acb-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="93acb-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93acb-122">Das Stammelement eines Microsoft Visio-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="93acb-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="93acb-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93acb-123">Child elements</span></span>

|<span data-ttu-id="93acb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="93acb-124">**Element**</span></span>|<span data-ttu-id="93acb-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="93acb-125">**Type**</span></span>|<span data-ttu-id="93acb-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93acb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93acb-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="93acb-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93acb-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="93acb-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93acb-129">Repräsentiert eine in einem Dokument definierte Formatvorlage.</span><span class="sxs-lookup"><span data-stu-id="93acb-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="93acb-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="93acb-130">Attributes</span></span>

<span data-ttu-id="93acb-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="93acb-131">None.</span></span>
  

