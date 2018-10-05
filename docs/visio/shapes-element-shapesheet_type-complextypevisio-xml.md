---
title: Shapes-Element (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Enthält eine Auflistung von Shape-Elementen.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392095"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="67917-103">Shapes-Element (ShapeSheet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="67917-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67917-104">Enthält eine Auflistung von Shape-Elementen.</span><span class="sxs-lookup"><span data-stu-id="67917-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67917-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="67917-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67917-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="67917-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67917-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="67917-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67917-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67917-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67917-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="67917-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67917-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67917-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67917-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="67917-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67917-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="67917-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67917-113">Definition</span><span class="sxs-lookup"><span data-stu-id="67917-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67917-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="67917-114">Elements and attributes</span></span>

<span data-ttu-id="67917-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="67917-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67917-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67917-116">Parent elements</span></span>

|<span data-ttu-id="67917-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="67917-117">**Element**</span></span>|<span data-ttu-id="67917-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="67917-118">**Type**</span></span>|<span data-ttu-id="67917-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67917-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67917-120">Shape</span><span class="sxs-lookup"><span data-stu-id="67917-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67917-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="67917-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67917-122">Gibt eine Auflistung von Eigenschaften, die mit einer Form verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="67917-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67917-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67917-123">Child elements</span></span>

|<span data-ttu-id="67917-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="67917-124">**Element**</span></span>|<span data-ttu-id="67917-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="67917-125">**Type**</span></span>|<span data-ttu-id="67917-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67917-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67917-127">Shape</span><span class="sxs-lookup"><span data-stu-id="67917-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67917-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="67917-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67917-129">Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="67917-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="67917-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="67917-130">Attributes</span></span>

<span data-ttu-id="67917-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="67917-131">None.</span></span>
  

