---
title: Data2-Element (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Enthält einen beliebigen Zeichenfolgenwert, der zum Angeben zusätzlicher Informationen zu einem Shape verwendet wird.
ms.openlocfilehash: f76300d67cd973850abc529ed5790b581e8c0ef4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542464"
---
# <a name="data2-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="9dc7f-103">Data2-Element (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9dc7f-103">Data2 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9dc7f-104">Enthält einen beliebigen Zeichenfolgenwert, der zum Angeben zusätzlicher Informationen zu einem Shape verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dc7f-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dc7f-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9dc7f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dc7f-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9dc7f-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="9dc7f-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9dc7f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9dc7f-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9dc7f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9dc7f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9dc7f-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9dc7f-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="9dc7f-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dc7f-113">Definition</span><span class="sxs-lookup"><span data-stu-id="9dc7f-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9dc7f-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9dc7f-114">Elements and attributes</span></span>

<span data-ttu-id="9dc7f-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9dc7f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9dc7f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9dc7f-116">Parent elements</span></span>

|<span data-ttu-id="9dc7f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-117">**Element**</span></span>|<span data-ttu-id="9dc7f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-118">**Type**</span></span>|<span data-ttu-id="9dc7f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dc7f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dc7f-120">Shape</span><span class="sxs-lookup"><span data-stu-id="9dc7f-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9dc7f-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9dc7f-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9dc7f-122">Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppenformelement definieren.</span><span class="sxs-lookup"><span data-stu-id="9dc7f-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9dc7f-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9dc7f-123">Child elements</span></span>

<span data-ttu-id="9dc7f-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="9dc7f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dc7f-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="9dc7f-125">Attributes</span></span>

<span data-ttu-id="9dc7f-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="9dc7f-126">None.</span></span>
  

