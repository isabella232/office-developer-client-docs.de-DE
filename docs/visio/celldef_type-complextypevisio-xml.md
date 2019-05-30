---
title: CellDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542296"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="f1ea1-102">CellDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1ea1-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f1ea1-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="f1ea1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1ea1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f1ea1-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f1ea1-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f1ea1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f1ea1-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f1ea1-108">Keine</span><span class="sxs-lookup"><span data-stu-id="f1ea1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1ea1-109">Definition</span><span class="sxs-lookup"><span data-stu-id="f1ea1-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1ea1-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="f1ea1-110">Elements and attributes</span></span>

<span data-ttu-id="f1ea1-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f1ea1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1ea1-112">Child elements</span></span>

<span data-ttu-id="f1ea1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1ea1-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1ea1-114">Attributes</span></span>

|<span data-ttu-id="f1ea1-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-115">**Attribute**</span></span>|<span data-ttu-id="f1ea1-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-116">**Type**</span></span>|<span data-ttu-id="f1ea1-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-117">**Required**</span></span>|<span data-ttu-id="f1ea1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-118">**Description**</span></span>|<span data-ttu-id="f1ea1-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="f1ea1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1ea1-120">F</span><span class="sxs-lookup"><span data-stu-id="f1ea1-120">F</span></span>  <br/> |<span data-ttu-id="f1ea1-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1ea1-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f1ea1-122">Optional</span><span class="sxs-lookup"><span data-stu-id="f1ea1-122">optional</span></span>  <br/> ||<span data-ttu-id="f1ea1-123">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f1ea1-124">IX</span><span class="sxs-lookup"><span data-stu-id="f1ea1-124">IX</span></span>  <br/> |<span data-ttu-id="f1ea1-125">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f1ea1-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="f1ea1-126">Optional</span><span class="sxs-lookup"><span data-stu-id="f1ea1-126">optional</span></span>  <br/> ||<span data-ttu-id="f1ea1-127">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="f1ea1-128">N</span><span class="sxs-lookup"><span data-stu-id="f1ea1-128">N</span></span>  <br/> |<span data-ttu-id="f1ea1-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f1ea1-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f1ea1-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f1ea1-130">required</span></span>  <br/> ||<span data-ttu-id="f1ea1-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f1ea1-132">S</span><span class="sxs-lookup"><span data-stu-id="f1ea1-132">S</span></span>  <br/> |<span data-ttu-id="f1ea1-133">XSD: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f1ea1-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="f1ea1-134">Optional</span><span class="sxs-lookup"><span data-stu-id="f1ea1-134">optional</span></span>  <br/> ||<span data-ttu-id="f1ea1-135">Werte des XSD: unsignedByte-Typs.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="f1ea1-136">T</span><span class="sxs-lookup"><span data-stu-id="f1ea1-136">T</span></span>  <br/> |<span data-ttu-id="f1ea1-137">XSD: Token</span><span class="sxs-lookup"><span data-stu-id="f1ea1-137">xsd:token</span></span>  <br/> |<span data-ttu-id="f1ea1-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="f1ea1-138">required</span></span>  <br/> ||<span data-ttu-id="f1ea1-139">Werte des XSD: Token-Typs.</span><span class="sxs-lookup"><span data-stu-id="f1ea1-139">Values of the xsd:token type.</span></span>  <br/> |
   

