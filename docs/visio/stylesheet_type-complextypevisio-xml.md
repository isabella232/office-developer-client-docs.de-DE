---
title: StyleSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541981"
---
# <a name="stylesheet_type-complextype-visio-xml"></a><span data-ttu-id="2c7b2-102">StyleSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2c7b2-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2c7b2-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2c7b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c7b2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2c7b2-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2c7b2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2c7b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2c7b2-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2c7b2-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="2c7b2-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2c7b2-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2c7b2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2c7b2-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2c7b2-110">Elements and attributes</span></span>

<span data-ttu-id="2c7b2-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2c7b2-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c7b2-112">Child elements</span></span>

<span data-ttu-id="2c7b2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c7b2-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c7b2-114">Attributes</span></span>

|<span data-ttu-id="2c7b2-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-115">**Attribute**</span></span>|<span data-ttu-id="2c7b2-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-116">**Type**</span></span>|<span data-ttu-id="2c7b2-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-117">**Required**</span></span>|<span data-ttu-id="2c7b2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-118">**Description**</span></span>|<span data-ttu-id="2c7b2-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="2c7b2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2c7b2-120">ID</span><span class="sxs-lookup"><span data-stu-id="2c7b2-120">ID</span></span>  <br/> |<span data-ttu-id="2c7b2-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2c7b2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2c7b2-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="2c7b2-122">required</span></span>  <br/> ||<span data-ttu-id="2c7b2-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2c7b2-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2c7b2-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="2c7b2-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2c7b2-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2c7b2-126">Optional</span><span class="sxs-lookup"><span data-stu-id="2c7b2-126">optional</span></span>  <br/> ||<span data-ttu-id="2c7b2-127">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2c7b2-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2c7b2-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2c7b2-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2c7b2-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2c7b2-130">Optional</span><span class="sxs-lookup"><span data-stu-id="2c7b2-130">optional</span></span>  <br/> ||<span data-ttu-id="2c7b2-131">Werte des typs xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2c7b2-132">Name</span><span class="sxs-lookup"><span data-stu-id="2c7b2-132">Name</span></span>  <br/> |<span data-ttu-id="2c7b2-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c7b2-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2c7b2-134">Optional</span><span class="sxs-lookup"><span data-stu-id="2c7b2-134">optional</span></span>  <br/> ||<span data-ttu-id="2c7b2-135">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2c7b2-136">NameU</span><span class="sxs-lookup"><span data-stu-id="2c7b2-136">NameU</span></span>  <br/> |<span data-ttu-id="2c7b2-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c7b2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2c7b2-138">Optional</span><span class="sxs-lookup"><span data-stu-id="2c7b2-138">optional</span></span>  <br/> ||<span data-ttu-id="2c7b2-139">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="2c7b2-139">Values of the xsd:string type.</span></span>  <br/> |
   

