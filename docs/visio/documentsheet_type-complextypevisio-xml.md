---
title: DocumentSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326138"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="6c157-102">DocumentSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6c157-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6c157-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6c157-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c157-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c157-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c157-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6c157-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c157-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6c157-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c157-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6c157-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c157-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="6c157-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c157-109">Definition</span><span class="sxs-lookup"><span data-stu-id="6c157-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c157-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6c157-110">Elements and attributes</span></span>

<span data-ttu-id="6c157-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6c157-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c157-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6c157-112">Child elements</span></span>

<span data-ttu-id="6c157-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="6c157-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c157-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="6c157-114">Attributes</span></span>

|<span data-ttu-id="6c157-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6c157-115">**Attribute**</span></span>|<span data-ttu-id="6c157-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6c157-116">**Type**</span></span>|<span data-ttu-id="6c157-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6c157-117">**Required**</span></span>|<span data-ttu-id="6c157-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c157-118">**Description**</span></span>|<span data-ttu-id="6c157-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6c157-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c157-120">IsCustomname</span><span class="sxs-lookup"><span data-stu-id="6c157-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="6c157-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6c157-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6c157-122">Optional</span><span class="sxs-lookup"><span data-stu-id="6c157-122">optional</span></span>  <br/> ||<span data-ttu-id="6c157-123">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="6c157-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6c157-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6c157-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6c157-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6c157-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6c157-126">Optional</span><span class="sxs-lookup"><span data-stu-id="6c157-126">optional</span></span>  <br/> ||<span data-ttu-id="6c157-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="6c157-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6c157-128">Name</span><span class="sxs-lookup"><span data-stu-id="6c157-128">Name</span></span>  <br/> |<span data-ttu-id="6c157-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6c157-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6c157-130">Optional</span><span class="sxs-lookup"><span data-stu-id="6c157-130">optional</span></span>  <br/> ||<span data-ttu-id="6c157-131">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="6c157-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c157-132">NameU</span><span class="sxs-lookup"><span data-stu-id="6c157-132">NameU</span></span>  <br/> |<span data-ttu-id="6c157-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6c157-133">xsd:string</span></span>  <br/> |<span data-ttu-id="6c157-134">Optional</span><span class="sxs-lookup"><span data-stu-id="6c157-134">optional</span></span>  <br/> ||<span data-ttu-id="6c157-135">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="6c157-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c157-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="6c157-136">UniqueID</span></span>  <br/> |<span data-ttu-id="6c157-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6c157-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6c157-138">Optional</span><span class="sxs-lookup"><span data-stu-id="6c157-138">optional</span></span>  <br/> ||<span data-ttu-id="6c157-139">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="6c157-139">Values of the xsd:string type.</span></span>  <br/> |
   

