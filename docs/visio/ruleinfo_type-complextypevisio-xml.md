---
title: RuleInfo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541645"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="5316b-102">RuleInfo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5316b-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5316b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5316b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5316b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5316b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5316b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5316b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5316b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="5316b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5316b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5316b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5316b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="5316b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5316b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5316b-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5316b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5316b-110">Elements and attributes</span></span>

<span data-ttu-id="5316b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="5316b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5316b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5316b-112">Child elements</span></span>

<span data-ttu-id="5316b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5316b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5316b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5316b-114">Attributes</span></span>

|<span data-ttu-id="5316b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5316b-115">**Attribute**</span></span>|<span data-ttu-id="5316b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5316b-116">**Type**</span></span>|<span data-ttu-id="5316b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="5316b-117">**Required**</span></span>|<span data-ttu-id="5316b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5316b-118">**Description**</span></span>|<span data-ttu-id="5316b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="5316b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5316b-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="5316b-120">RuleID</span></span>  <br/> |<span data-ttu-id="5316b-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5316b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5316b-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5316b-122">required</span></span>  <br/> ||<span data-ttu-id="5316b-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5316b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5316b-124">RuleSet</span><span class="sxs-lookup"><span data-stu-id="5316b-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="5316b-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5316b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5316b-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="5316b-126">required</span></span>  <br/> ||<span data-ttu-id="5316b-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="5316b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

