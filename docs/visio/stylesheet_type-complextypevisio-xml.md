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
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="57c54-102">StyleSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="57c54-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="57c54-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="57c54-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57c54-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="57c54-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57c54-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="57c54-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57c54-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="57c54-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57c54-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="57c54-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57c54-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="57c54-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57c54-109">Definition</span><span class="sxs-lookup"><span data-stu-id="57c54-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="57c54-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="57c54-110">Elements and attributes</span></span>

<span data-ttu-id="57c54-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="57c54-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57c54-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57c54-112">Child elements</span></span>

<span data-ttu-id="57c54-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="57c54-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57c54-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="57c54-114">Attributes</span></span>

|<span data-ttu-id="57c54-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="57c54-115">**Attribute**</span></span>|<span data-ttu-id="57c54-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="57c54-116">**Type**</span></span>|<span data-ttu-id="57c54-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="57c54-117">**Required**</span></span>|<span data-ttu-id="57c54-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57c54-118">**Description**</span></span>|<span data-ttu-id="57c54-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="57c54-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="57c54-120">ID</span><span class="sxs-lookup"><span data-stu-id="57c54-120">ID</span></span>  <br/> |<span data-ttu-id="57c54-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="57c54-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="57c54-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="57c54-122">required</span></span>  <br/> ||<span data-ttu-id="57c54-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="57c54-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="57c54-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="57c54-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="57c54-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="57c54-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="57c54-126">Optional</span><span class="sxs-lookup"><span data-stu-id="57c54-126">optional</span></span>  <br/> ||<span data-ttu-id="57c54-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="57c54-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="57c54-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="57c54-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="57c54-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="57c54-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="57c54-130">Optional</span><span class="sxs-lookup"><span data-stu-id="57c54-130">optional</span></span>  <br/> ||<span data-ttu-id="57c54-131">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="57c54-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="57c54-132">Name</span><span class="sxs-lookup"><span data-stu-id="57c54-132">Name</span></span>  <br/> |<span data-ttu-id="57c54-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="57c54-133">xsd:string</span></span>  <br/> |<span data-ttu-id="57c54-134">Optional</span><span class="sxs-lookup"><span data-stu-id="57c54-134">optional</span></span>  <br/> ||<span data-ttu-id="57c54-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="57c54-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="57c54-136">NameU</span><span class="sxs-lookup"><span data-stu-id="57c54-136">NameU</span></span>  <br/> |<span data-ttu-id="57c54-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="57c54-137">xsd:string</span></span>  <br/> |<span data-ttu-id="57c54-138">Optional</span><span class="sxs-lookup"><span data-stu-id="57c54-138">optional</span></span>  <br/> ||<span data-ttu-id="57c54-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="57c54-139">Values of the xsd:string type.</span></span>  <br/> |
   

