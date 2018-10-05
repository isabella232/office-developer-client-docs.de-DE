---
title: Data1-Element (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.
ms.openlocfilehash: a203f915e9a5ff86e7cf75d96639157f76d3c151
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390968"
---
# <a name="data1-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="e09a6-103">Data1-Element (ShapeSheet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="e09a6-103">Data1 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e09a6-104">Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e09a6-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e09a6-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e09a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e09a6-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="e09a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e09a6-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e09a6-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e09a6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e09a6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e09a6-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e09a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e09a6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e09a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e09a6-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="e09a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e09a6-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="e09a6-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e09a6-113">Definition</span><span class="sxs-lookup"><span data-stu-id="e09a6-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e09a6-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e09a6-114">Elements and attributes</span></span>

<span data-ttu-id="e09a6-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e09a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e09a6-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e09a6-116">Parent elements</span></span>

|<span data-ttu-id="e09a6-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e09a6-117">**Element**</span></span>|<span data-ttu-id="e09a6-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e09a6-118">**Type**</span></span>|<span data-ttu-id="e09a6-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e09a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e09a6-120">Shape</span><span class="sxs-lookup"><span data-stu-id="e09a6-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e09a6-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e09a6-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e09a6-122">Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="e09a6-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e09a6-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e09a6-123">Child elements</span></span>

<span data-ttu-id="e09a6-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="e09a6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e09a6-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="e09a6-125">Attributes</span></span>

<span data-ttu-id="e09a6-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="e09a6-126">None.</span></span>
  

