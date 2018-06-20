---
title: Shapes-Element (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Enthält eine Auflistung von Shape-Elementen.
ms.openlocfilehash: d2e725a28873cac8dded49587a98400df1d9bf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798050"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="bcdcf-103">Shapes-Element (ShapeSheet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bcdcf-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="bcdcf-104">Enthält eine Auflistung von Shape-Elementen.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcdcf-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bcdcf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcdcf-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bcdcf-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="bcdcf-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bcdcf-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bcdcf-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bcdcf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bcdcf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bcdcf-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bcdcf-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="bcdcf-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bcdcf-113">Definition</span><span class="sxs-lookup"><span data-stu-id="bcdcf-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bcdcf-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bcdcf-114">Elements and attributes</span></span>

<span data-ttu-id="bcdcf-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bcdcf-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bcdcf-116">Parent elements</span></span>

|<span data-ttu-id="bcdcf-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-117">**Element**</span></span>|<span data-ttu-id="bcdcf-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-118">**Type**</span></span>|<span data-ttu-id="bcdcf-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcdcf-120">Shape</span><span class="sxs-lookup"><span data-stu-id="bcdcf-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bcdcf-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bcdcf-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcdcf-122">Gibt eine Auflistung von Eigenschaften, die mit einer Form verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bcdcf-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bcdcf-123">Child elements</span></span>

|<span data-ttu-id="bcdcf-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-124">**Element**</span></span>|<span data-ttu-id="bcdcf-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-125">**Type**</span></span>|<span data-ttu-id="bcdcf-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bcdcf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcdcf-127">Shape</span><span class="sxs-lookup"><span data-stu-id="bcdcf-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bcdcf-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bcdcf-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcdcf-129">Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bcdcf-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="bcdcf-130">Attributes</span></span>

<span data-ttu-id="bcdcf-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="bcdcf-131">None.</span></span>
  

