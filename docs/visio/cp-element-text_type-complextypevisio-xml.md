---
title: cp-Element (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Markiert den Anfang einer Ausführung einer Zeicheneigenschaften, die gemäß dem entsprechenden Char-Element formatiert ist. Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540560"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="f6c7d-104">cp-Element (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f6c7d-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f6c7d-105">Markiert den Anfang einer Ausführung einer Zeicheneigenschaften, die gemäß dem entsprechenden Char-Element formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="f6c7d-106">Die Ausführung wird bis zum Ende des Texts oder bis zum nächsten Tag definiert.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6c7d-107">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f6c7d-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6c7d-108">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-108">**Element type**</span></span> <br/> |[<span data-ttu-id="f6c7d-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="f6c7d-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6c7d-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6c7d-111">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-111">**Schema file**</span></span> <br/> |<span data-ttu-id="f6c7d-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f6c7d-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6c7d-113">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-113">**Document parts**</span></span> <br/> |<span data-ttu-id="f6c7d-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="f6c7d-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f6c7d-115">Definition</span><span class="sxs-lookup"><span data-stu-id="f6c7d-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6c7d-116">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f6c7d-116">Elements and attributes</span></span>

<span data-ttu-id="f6c7d-117">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6c7d-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6c7d-118">Parent elements</span></span>

|<span data-ttu-id="f6c7d-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-119">**Element**</span></span>|<span data-ttu-id="f6c7d-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-120">**Type**</span></span>|<span data-ttu-id="f6c7d-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6c7d-122">Text</span><span class="sxs-lookup"><span data-stu-id="f6c7d-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f6c7d-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f6c7d-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6c7d-124">Enthält den Text einer Form.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6c7d-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6c7d-125">Child elements</span></span>

<span data-ttu-id="f6c7d-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6c7d-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6c7d-127">Attributes</span></span>

|<span data-ttu-id="f6c7d-128">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-128">**Attribute**</span></span>|<span data-ttu-id="f6c7d-129">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-129">**Type**</span></span>|<span data-ttu-id="f6c7d-130">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-130">**Required**</span></span>|<span data-ttu-id="f6c7d-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-131">**Description**</span></span>|<span data-ttu-id="f6c7d-132">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f6c7d-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6c7d-133">IX</span><span class="sxs-lookup"><span data-stu-id="f6c7d-133">IX</span></span>  <br/> |<span data-ttu-id="f6c7d-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f6c7d-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f6c7d-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f6c7d-135">required</span></span>  <br/> |<span data-ttu-id="f6c7d-136">Der Char-Elementindex, der von dieser Eigenschaft ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="f6c7d-137">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="f6c7d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

