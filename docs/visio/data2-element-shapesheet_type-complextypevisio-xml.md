---
title: Data2-Element (ShapeSheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.
ms.openlocfilehash: 9533f4b92cb73a6fc99ba82e2221eba40fb917b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796777"
---
# <a name="data2-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ac5a9-103">Data2-Element (ShapeSheet_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ac5a9-103">Data2 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ac5a9-104">Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ac5a9-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac5a9-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ac5a9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac5a9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ac5a9-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ac5a9-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ac5a9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ac5a9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ac5a9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ac5a9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ac5a9-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ac5a9-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="ac5a9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac5a9-113">Definition</span><span class="sxs-lookup"><span data-stu-id="ac5a9-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac5a9-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ac5a9-114">Elements and attributes</span></span>

<span data-ttu-id="ac5a9-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ac5a9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ac5a9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac5a9-116">Parent elements</span></span>

|<span data-ttu-id="ac5a9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-117">**Element**</span></span>|<span data-ttu-id="ac5a9-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-118">**Type**</span></span>|<span data-ttu-id="ac5a9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac5a9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac5a9-120">Shape</span><span class="sxs-lookup"><span data-stu-id="ac5a9-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ac5a9-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ac5a9-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ac5a9-122">Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.</span><span class="sxs-lookup"><span data-stu-id="ac5a9-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac5a9-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac5a9-123">Child elements</span></span>

<span data-ttu-id="ac5a9-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac5a9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac5a9-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac5a9-125">Attributes</span></span>

<span data-ttu-id="ac5a9-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac5a9-126">None.</span></span>
  

