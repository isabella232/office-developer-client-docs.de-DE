---
title: RuleInfo_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382568"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="ebd74-102">RuleInfo_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ebd74-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ebd74-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ebd74-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebd74-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ebd74-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ebd74-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ebd74-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ebd74-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ebd74-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ebd74-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ebd74-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ebd74-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ebd74-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ebd74-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ebd74-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ebd74-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ebd74-110">Elements and attributes</span></span>

<span data-ttu-id="ebd74-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ebd74-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ebd74-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebd74-112">Child elements</span></span>

<span data-ttu-id="ebd74-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ebd74-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebd74-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ebd74-114">Attributes</span></span>

|<span data-ttu-id="ebd74-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ebd74-115">**Attribute**</span></span>|<span data-ttu-id="ebd74-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ebd74-116">**Type**</span></span>|<span data-ttu-id="ebd74-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ebd74-117">**Required**</span></span>|<span data-ttu-id="ebd74-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebd74-118">**Description**</span></span>|<span data-ttu-id="ebd74-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ebd74-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ebd74-120">Regel-ID</span><span class="sxs-lookup"><span data-stu-id="ebd74-120">RuleID</span></span>  <br/> |<span data-ttu-id="ebd74-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ebd74-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ebd74-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd74-122">required</span></span>  <br/> ||<span data-ttu-id="ebd74-123">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ebd74-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ebd74-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="ebd74-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="ebd74-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ebd74-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ebd74-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ebd74-126">required</span></span>  <br/> ||<span data-ttu-id="ebd74-127">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ebd74-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

