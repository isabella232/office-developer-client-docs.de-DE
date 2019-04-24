---
title: RuleInfo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360466"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="58604-102">RuleInfo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="58604-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="58604-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="58604-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58604-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="58604-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="58604-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="58604-105">**Schema file**</span></span> <br/> |<span data-ttu-id="58604-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="58604-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="58604-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="58604-107">**Extension base**</span></span> <br/> |<span data-ttu-id="58604-108">Keine</span><span class="sxs-lookup"><span data-stu-id="58604-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58604-109">Definition</span><span class="sxs-lookup"><span data-stu-id="58604-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="58604-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="58604-110">Elements and attributes</span></span>

<span data-ttu-id="58604-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="58604-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="58604-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58604-112">Child elements</span></span>

<span data-ttu-id="58604-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="58604-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58604-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="58604-114">Attributes</span></span>

|<span data-ttu-id="58604-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="58604-115">**Attribute**</span></span>|<span data-ttu-id="58604-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="58604-116">**Type**</span></span>|<span data-ttu-id="58604-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="58604-117">**Required**</span></span>|<span data-ttu-id="58604-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58604-118">**Description**</span></span>|<span data-ttu-id="58604-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="58604-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58604-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="58604-120">RuleID</span></span>  <br/> |<span data-ttu-id="58604-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58604-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58604-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58604-122">required</span></span>  <br/> ||<span data-ttu-id="58604-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="58604-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58604-124">Regelsatz</span><span class="sxs-lookup"><span data-stu-id="58604-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="58604-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58604-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58604-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="58604-126">required</span></span>  <br/> ||<span data-ttu-id="58604-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="58604-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

