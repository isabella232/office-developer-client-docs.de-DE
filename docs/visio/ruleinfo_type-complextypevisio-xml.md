---
title: RuleInfo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797939"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="78a33-102">RuleInfo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="78a33-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="78a33-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="78a33-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78a33-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="78a33-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="78a33-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="78a33-105">**Schema file**</span></span> <br/> |<span data-ttu-id="78a33-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="78a33-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="78a33-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="78a33-107">**Extension base**</span></span> <br/> |<span data-ttu-id="78a33-108">Keine</span><span class="sxs-lookup"><span data-stu-id="78a33-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78a33-109">Definition</span><span class="sxs-lookup"><span data-stu-id="78a33-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="78a33-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="78a33-110">Elements and attributes</span></span>

<span data-ttu-id="78a33-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="78a33-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="78a33-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78a33-112">Child elements</span></span>

<span data-ttu-id="78a33-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="78a33-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78a33-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="78a33-114">Attributes</span></span>

|<span data-ttu-id="78a33-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="78a33-115">**Attribute**</span></span>|<span data-ttu-id="78a33-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="78a33-116">**Type**</span></span>|<span data-ttu-id="78a33-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="78a33-117">**Required**</span></span>|<span data-ttu-id="78a33-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78a33-118">**Description**</span></span>|<span data-ttu-id="78a33-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="78a33-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="78a33-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="78a33-120">RuleID</span></span>  <br/> |<span data-ttu-id="78a33-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="78a33-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="78a33-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="78a33-122">required</span></span>  <br/> ||<span data-ttu-id="78a33-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="78a33-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="78a33-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="78a33-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="78a33-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="78a33-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="78a33-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="78a33-126">required</span></span>  <br/> ||<span data-ttu-id="78a33-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="78a33-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

