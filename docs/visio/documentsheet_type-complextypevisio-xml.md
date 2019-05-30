---
title: DocumentSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540007"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="80a94-102">DocumentSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="80a94-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="80a94-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="80a94-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80a94-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80a94-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="80a94-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="80a94-105">**Schema file**</span></span> <br/> |<span data-ttu-id="80a94-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="80a94-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="80a94-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="80a94-107">**Extension base**</span></span> <br/> |<span data-ttu-id="80a94-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="80a94-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80a94-109">Definition</span><span class="sxs-lookup"><span data-stu-id="80a94-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="80a94-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="80a94-110">Elements and attributes</span></span>

<span data-ttu-id="80a94-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="80a94-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="80a94-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="80a94-112">Child elements</span></span>

<span data-ttu-id="80a94-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="80a94-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80a94-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="80a94-114">Attributes</span></span>

|<span data-ttu-id="80a94-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="80a94-115">**Attribute**</span></span>|<span data-ttu-id="80a94-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="80a94-116">**Type**</span></span>|<span data-ttu-id="80a94-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="80a94-117">**Required**</span></span>|<span data-ttu-id="80a94-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="80a94-118">**Description**</span></span>|<span data-ttu-id="80a94-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="80a94-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80a94-120">Iscustomname</span><span class="sxs-lookup"><span data-stu-id="80a94-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="80a94-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="80a94-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="80a94-122">Optional</span><span class="sxs-lookup"><span data-stu-id="80a94-122">optional</span></span>  <br/> ||<span data-ttu-id="80a94-123">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="80a94-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="80a94-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="80a94-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="80a94-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="80a94-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="80a94-126">Optional</span><span class="sxs-lookup"><span data-stu-id="80a94-126">optional</span></span>  <br/> ||<span data-ttu-id="80a94-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="80a94-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="80a94-128">Name</span><span class="sxs-lookup"><span data-stu-id="80a94-128">Name</span></span>  <br/> |<span data-ttu-id="80a94-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="80a94-129">xsd:string</span></span>  <br/> |<span data-ttu-id="80a94-130">Optional</span><span class="sxs-lookup"><span data-stu-id="80a94-130">optional</span></span>  <br/> ||<span data-ttu-id="80a94-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="80a94-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="80a94-132">NameU</span><span class="sxs-lookup"><span data-stu-id="80a94-132">NameU</span></span>  <br/> |<span data-ttu-id="80a94-133">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="80a94-133">xsd:string</span></span>  <br/> |<span data-ttu-id="80a94-134">Optional</span><span class="sxs-lookup"><span data-stu-id="80a94-134">optional</span></span>  <br/> ||<span data-ttu-id="80a94-135">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="80a94-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="80a94-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="80a94-136">UniqueID</span></span>  <br/> |<span data-ttu-id="80a94-137">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="80a94-137">xsd:string</span></span>  <br/> |<span data-ttu-id="80a94-138">Optional</span><span class="sxs-lookup"><span data-stu-id="80a94-138">optional</span></span>  <br/> ||<span data-ttu-id="80a94-139">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="80a94-139">Values of the xsd:string type.</span></span>  <br/> |
   

