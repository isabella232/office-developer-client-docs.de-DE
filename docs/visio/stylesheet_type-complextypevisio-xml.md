---
title: StyleSheet_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396001"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="3bb39-102">StyleSheet_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="3bb39-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3bb39-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="3bb39-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bb39-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3bb39-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3bb39-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3bb39-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3bb39-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3bb39-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3bb39-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="3bb39-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3bb39-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="3bb39-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3bb39-109">Definition</span><span class="sxs-lookup"><span data-stu-id="3bb39-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3bb39-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3bb39-110">Elements and attributes</span></span>

<span data-ttu-id="3bb39-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="3bb39-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3bb39-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3bb39-112">Child elements</span></span>

<span data-ttu-id="3bb39-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3bb39-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bb39-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="3bb39-114">Attributes</span></span>

|<span data-ttu-id="3bb39-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3bb39-115">**Attribute**</span></span>|<span data-ttu-id="3bb39-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3bb39-116">**Type**</span></span>|<span data-ttu-id="3bb39-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="3bb39-117">**Required**</span></span>|<span data-ttu-id="3bb39-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3bb39-118">**Description**</span></span>|<span data-ttu-id="3bb39-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="3bb39-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3bb39-120">ID</span><span class="sxs-lookup"><span data-stu-id="3bb39-120">ID</span></span>  <br/> |<span data-ttu-id="3bb39-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3bb39-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3bb39-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="3bb39-122">required</span></span>  <br/> ||<span data-ttu-id="3bb39-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3bb39-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3bb39-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="3bb39-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="3bb39-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3bb39-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3bb39-126">Optional</span><span class="sxs-lookup"><span data-stu-id="3bb39-126">optional</span></span>  <br/> ||<span data-ttu-id="3bb39-127">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3bb39-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3bb39-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="3bb39-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="3bb39-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3bb39-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3bb39-130">Optional</span><span class="sxs-lookup"><span data-stu-id="3bb39-130">optional</span></span>  <br/> ||<span data-ttu-id="3bb39-131">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3bb39-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3bb39-132">Name</span><span class="sxs-lookup"><span data-stu-id="3bb39-132">Name</span></span>  <br/> |<span data-ttu-id="3bb39-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3bb39-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3bb39-134">Optional</span><span class="sxs-lookup"><span data-stu-id="3bb39-134">optional</span></span>  <br/> ||<span data-ttu-id="3bb39-135">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3bb39-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3bb39-136">NameU</span><span class="sxs-lookup"><span data-stu-id="3bb39-136">NameU</span></span>  <br/> |<span data-ttu-id="3bb39-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="3bb39-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3bb39-138">Optional</span><span class="sxs-lookup"><span data-stu-id="3bb39-138">optional</span></span>  <br/> ||<span data-ttu-id="3bb39-139">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3bb39-139">Values of the xsd:string type.</span></span>  <br/> |
   

