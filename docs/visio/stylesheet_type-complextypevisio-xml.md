---
title: StyleSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798221"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="c82de-102">StyleSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c82de-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c82de-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c82de-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c82de-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c82de-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c82de-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c82de-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c82de-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c82de-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c82de-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c82de-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c82de-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="c82de-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c82de-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c82de-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c82de-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c82de-110">Elements and attributes</span></span>

<span data-ttu-id="c82de-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c82de-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c82de-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c82de-112">Child elements</span></span>

<span data-ttu-id="c82de-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c82de-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c82de-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="c82de-114">Attributes</span></span>

|<span data-ttu-id="c82de-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c82de-115">**Attribute**</span></span>|<span data-ttu-id="c82de-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c82de-116">**Type**</span></span>|<span data-ttu-id="c82de-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c82de-117">**Required**</span></span>|<span data-ttu-id="c82de-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c82de-118">**Description**</span></span>|<span data-ttu-id="c82de-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="c82de-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c82de-120">ID</span><span class="sxs-lookup"><span data-stu-id="c82de-120">ID</span></span>  <br/> |<span data-ttu-id="c82de-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c82de-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c82de-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="c82de-122">required</span></span>  <br/> ||<span data-ttu-id="c82de-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c82de-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c82de-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c82de-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="c82de-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c82de-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c82de-126">Optional</span><span class="sxs-lookup"><span data-stu-id="c82de-126">optional</span></span>  <br/> ||<span data-ttu-id="c82de-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c82de-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c82de-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c82de-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c82de-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c82de-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c82de-130">Optional</span><span class="sxs-lookup"><span data-stu-id="c82de-130">optional</span></span>  <br/> ||<span data-ttu-id="c82de-131">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c82de-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c82de-132">Name</span><span class="sxs-lookup"><span data-stu-id="c82de-132">Name</span></span>  <br/> |<span data-ttu-id="c82de-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c82de-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c82de-134">Optional</span><span class="sxs-lookup"><span data-stu-id="c82de-134">optional</span></span>  <br/> ||<span data-ttu-id="c82de-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c82de-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c82de-136">NameU</span><span class="sxs-lookup"><span data-stu-id="c82de-136">NameU</span></span>  <br/> |<span data-ttu-id="c82de-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="c82de-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c82de-138">Optional</span><span class="sxs-lookup"><span data-stu-id="c82de-138">optional</span></span>  <br/> ||<span data-ttu-id="c82de-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c82de-139">Values of the xsd:string type.</span></span>  <br/> |
   

