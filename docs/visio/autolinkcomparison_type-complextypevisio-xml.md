---
title: AutoLinkComparison_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537885"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="b1fab-102">AutoLinkComparison_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b1fab-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b1fab-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="b1fab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1fab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b1fab-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b1fab-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="b1fab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b1fab-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b1fab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b1fab-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="b1fab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b1fab-108">Keine</span><span class="sxs-lookup"><span data-stu-id="b1fab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b1fab-109">Definition</span><span class="sxs-lookup"><span data-stu-id="b1fab-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b1fab-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="b1fab-110">Elements and attributes</span></span>

<span data-ttu-id="b1fab-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="b1fab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b1fab-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b1fab-112">Child elements</span></span>

<span data-ttu-id="b1fab-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b1fab-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1fab-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b1fab-114">Attributes</span></span>

|<span data-ttu-id="b1fab-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b1fab-115">**Attribute**</span></span>|<span data-ttu-id="b1fab-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b1fab-116">**Type**</span></span>|<span data-ttu-id="b1fab-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="b1fab-117">**Required**</span></span>|<span data-ttu-id="b1fab-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b1fab-118">**Description**</span></span>|<span data-ttu-id="b1fab-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="b1fab-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b1fab-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="b1fab-120">ColumnName</span></span>  <br/> |<span data-ttu-id="b1fab-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1fab-121">xsd:string</span></span>  <br/> |<span data-ttu-id="b1fab-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b1fab-122">required</span></span>  <br/> ||<span data-ttu-id="b1fab-123">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b1fab-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b1fab-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="b1fab-124">ContextType</span></span>  <br/> |<span data-ttu-id="b1fab-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b1fab-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b1fab-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="b1fab-126">required</span></span>  <br/> ||<span data-ttu-id="b1fab-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="b1fab-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b1fab-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="b1fab-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="b1fab-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b1fab-129">xsd:string</span></span>  <br/> |<span data-ttu-id="b1fab-130">Optional</span><span class="sxs-lookup"><span data-stu-id="b1fab-130">optional</span></span>  <br/> ||<span data-ttu-id="b1fab-131">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b1fab-131">Values of the xsd:string type.</span></span>  <br/> |
   

