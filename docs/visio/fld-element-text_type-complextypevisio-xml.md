---
title: fld-Element (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Gibt eine Textfeldeinfügemarke für das entsprechende Field-Element an.
ms.openlocfilehash: efacb7ed11968dec5d5c2f62b0ca3e3bcd8580c0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539614"
---
# <a name="fld-element-text_type-complextype-visio-xml"></a><span data-ttu-id="3bfdc-103">fld-Element (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3bfdc-103">fld element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3bfdc-104">Gibt eine Textfeldeinfügemarke für das entsprechende **Field-Element** an.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3bfdc-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3bfdc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bfdc-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3bfdc-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="3bfdc-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3bfdc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3bfdc-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3bfdc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3bfdc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3bfdc-111">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3bfdc-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="3bfdc-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3bfdc-113">Definition</span><span class="sxs-lookup"><span data-stu-id="3bfdc-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3bfdc-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3bfdc-114">Elements and attributes</span></span>

<span data-ttu-id="3bfdc-115">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3bfdc-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bfdc-116">Parent elements</span></span>

|<span data-ttu-id="3bfdc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-117">**Element**</span></span>|<span data-ttu-id="3bfdc-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-118">**Type**</span></span>|<span data-ttu-id="3bfdc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3bfdc-120">Text</span><span class="sxs-lookup"><span data-stu-id="3bfdc-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3bfdc-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="3bfdc-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3bfdc-122">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3bfdc-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bfdc-123">Child elements</span></span>

<span data-ttu-id="3bfdc-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bfdc-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="3bfdc-125">Attributes</span></span>

|<span data-ttu-id="3bfdc-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-126">**Attribute**</span></span>|<span data-ttu-id="3bfdc-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-127">**Type**</span></span>|<span data-ttu-id="3bfdc-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-128">**Required**</span></span>|<span data-ttu-id="3bfdc-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-129">**Description**</span></span>|<span data-ttu-id="3bfdc-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3bfdc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3bfdc-131">IX</span><span class="sxs-lookup"><span data-stu-id="3bfdc-131">IX</span></span>  <br/> |<span data-ttu-id="3bfdc-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bfdc-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bfdc-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3bfdc-133">required</span></span>  <br/> |<span data-ttu-id="3bfdc-134">Der nullbasierte Index des Elements innerhalb des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="3bfdc-135">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="3bfdc-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

