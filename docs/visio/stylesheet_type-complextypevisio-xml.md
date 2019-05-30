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
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="62457-102">StyleSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="62457-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="62457-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="62457-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62457-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62457-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="62457-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="62457-105">**Schema file**</span></span> <br/> |<span data-ttu-id="62457-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="62457-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="62457-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="62457-107">**Extension base**</span></span> <br/> |<span data-ttu-id="62457-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="62457-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62457-109">Definition</span><span class="sxs-lookup"><span data-stu-id="62457-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="62457-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="62457-110">Elements and attributes</span></span>

<span data-ttu-id="62457-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="62457-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62457-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62457-112">Child elements</span></span>

<span data-ttu-id="62457-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="62457-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62457-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="62457-114">Attributes</span></span>

|<span data-ttu-id="62457-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="62457-115">**Attribute**</span></span>|<span data-ttu-id="62457-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="62457-116">**Type**</span></span>|<span data-ttu-id="62457-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="62457-117">**Required**</span></span>|<span data-ttu-id="62457-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62457-118">**Description**</span></span>|<span data-ttu-id="62457-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="62457-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62457-120">ID</span><span class="sxs-lookup"><span data-stu-id="62457-120">ID</span></span>  <br/> |<span data-ttu-id="62457-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="62457-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62457-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="62457-122">required</span></span>  <br/> ||<span data-ttu-id="62457-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="62457-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="62457-124">Iscustomname</span><span class="sxs-lookup"><span data-stu-id="62457-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="62457-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="62457-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62457-126">Optional</span><span class="sxs-lookup"><span data-stu-id="62457-126">optional</span></span>  <br/> ||<span data-ttu-id="62457-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="62457-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="62457-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="62457-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="62457-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="62457-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62457-130">Optional</span><span class="sxs-lookup"><span data-stu-id="62457-130">optional</span></span>  <br/> ||<span data-ttu-id="62457-131">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="62457-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="62457-132">Name</span><span class="sxs-lookup"><span data-stu-id="62457-132">Name</span></span>  <br/> |<span data-ttu-id="62457-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="62457-133">xsd:string</span></span>  <br/> |<span data-ttu-id="62457-134">Optional</span><span class="sxs-lookup"><span data-stu-id="62457-134">optional</span></span>  <br/> ||<span data-ttu-id="62457-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="62457-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62457-136">NameU</span><span class="sxs-lookup"><span data-stu-id="62457-136">NameU</span></span>  <br/> |<span data-ttu-id="62457-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="62457-137">xsd:string</span></span>  <br/> |<span data-ttu-id="62457-138">Optional</span><span class="sxs-lookup"><span data-stu-id="62457-138">optional</span></span>  <br/> ||<span data-ttu-id="62457-139">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="62457-139">Values of the xsd:string type.</span></span>  <br/> |
   

