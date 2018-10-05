---
title: Fld-Element (Text_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Gibt ein Text-Feld Einfügemarke für die entsprechenden Field-Element an.
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383324"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="fb32e-103">Fld-Element (Text_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fb32e-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fb32e-104">Gibt ein Text-Feld Einfügemarke für die entsprechenden **Field** -Element an.</span><span class="sxs-lookup"><span data-stu-id="fb32e-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fb32e-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fb32e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb32e-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="fb32e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fb32e-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="fb32e-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fb32e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb32e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fb32e-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fb32e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fb32e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fb32e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fb32e-111">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="fb32e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fb32e-112">Seite # .xml, Gestaltungsvorlagen # .xml</span><span class="sxs-lookup"><span data-stu-id="fb32e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb32e-113">Definition</span><span class="sxs-lookup"><span data-stu-id="fb32e-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fb32e-114">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fb32e-114">Elements and attributes</span></span>

<span data-ttu-id="fb32e-115">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="fb32e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fb32e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb32e-116">Parent elements</span></span>

|<span data-ttu-id="fb32e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb32e-117">**Element**</span></span>|<span data-ttu-id="fb32e-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fb32e-118">**Type**</span></span>|<span data-ttu-id="fb32e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb32e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb32e-120">Text</span><span class="sxs-lookup"><span data-stu-id="fb32e-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb32e-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="fb32e-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb32e-122">Enthält den Text eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="fb32e-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb32e-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fb32e-123">Child elements</span></span>

<span data-ttu-id="fb32e-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="fb32e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb32e-125">Attribute</span><span class="sxs-lookup"><span data-stu-id="fb32e-125">Attributes</span></span>

|<span data-ttu-id="fb32e-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fb32e-126">**Attribute**</span></span>|<span data-ttu-id="fb32e-127">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fb32e-127">**Type**</span></span>|<span data-ttu-id="fb32e-128">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="fb32e-128">**Required**</span></span>|<span data-ttu-id="fb32e-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fb32e-129">**Description**</span></span>|<span data-ttu-id="fb32e-130">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="fb32e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb32e-131">IX</span><span class="sxs-lookup"><span data-stu-id="fb32e-131">IX</span></span>  <br/> |<span data-ttu-id="fb32e-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fb32e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fb32e-133">erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb32e-133">required</span></span>  <br/> |<span data-ttu-id="fb32e-134">Der nullbasierte Index des Elements in seinem übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="fb32e-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="fb32e-135">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fb32e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

