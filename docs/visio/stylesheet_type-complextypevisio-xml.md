---
title: StyleSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329825"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="20564-102">StyleSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="20564-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="20564-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="20564-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20564-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20564-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="20564-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="20564-105">**Schema file**</span></span> <br/> |<span data-ttu-id="20564-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="20564-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="20564-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="20564-107">**Extension base**</span></span> <br/> |<span data-ttu-id="20564-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="20564-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20564-109">Definition</span><span class="sxs-lookup"><span data-stu-id="20564-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="20564-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="20564-110">Elements and attributes</span></span>

<span data-ttu-id="20564-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="20564-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="20564-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20564-112">Child elements</span></span>

<span data-ttu-id="20564-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="20564-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20564-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="20564-114">Attributes</span></span>

|<span data-ttu-id="20564-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="20564-115">**Attribute**</span></span>|<span data-ttu-id="20564-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="20564-116">**Type**</span></span>|<span data-ttu-id="20564-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="20564-117">**Required**</span></span>|<span data-ttu-id="20564-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20564-118">**Description**</span></span>|<span data-ttu-id="20564-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="20564-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20564-120">ID</span><span class="sxs-lookup"><span data-stu-id="20564-120">ID</span></span>  <br/> |<span data-ttu-id="20564-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20564-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20564-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="20564-122">required</span></span>  <br/> ||<span data-ttu-id="20564-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="20564-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20564-124">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="20564-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="20564-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="20564-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="20564-126">Optional</span><span class="sxs-lookup"><span data-stu-id="20564-126">optional</span></span>  <br/> ||<span data-ttu-id="20564-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="20564-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="20564-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="20564-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="20564-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="20564-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="20564-130">Optional</span><span class="sxs-lookup"><span data-stu-id="20564-130">optional</span></span>  <br/> ||<span data-ttu-id="20564-131">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="20564-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="20564-132">Name</span><span class="sxs-lookup"><span data-stu-id="20564-132">Name</span></span>  <br/> |<span data-ttu-id="20564-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="20564-133">xsd:string</span></span>  <br/> |<span data-ttu-id="20564-134">Optional</span><span class="sxs-lookup"><span data-stu-id="20564-134">optional</span></span>  <br/> ||<span data-ttu-id="20564-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="20564-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20564-136">NameU</span><span class="sxs-lookup"><span data-stu-id="20564-136">NameU</span></span>  <br/> |<span data-ttu-id="20564-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="20564-137">xsd:string</span></span>  <br/> |<span data-ttu-id="20564-138">Optional</span><span class="sxs-lookup"><span data-stu-id="20564-138">optional</span></span>  <br/> ||<span data-ttu-id="20564-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="20564-139">Values of the xsd:string type.</span></span>  <br/> |
   

