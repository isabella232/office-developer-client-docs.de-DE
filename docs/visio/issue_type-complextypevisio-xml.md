---
title: Issue_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: f0346c20e4a290819e3f23a0384a59b308a5e907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797277"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="aa395-102">Issue_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="aa395-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aa395-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="aa395-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa395-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aa395-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aa395-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="aa395-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aa395-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aa395-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aa395-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="aa395-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aa395-108">Keine</span><span class="sxs-lookup"><span data-stu-id="aa395-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa395-109">Definition</span><span class="sxs-lookup"><span data-stu-id="aa395-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aa395-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="aa395-110">Elements and attributes</span></span>

<span data-ttu-id="aa395-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="aa395-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aa395-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aa395-112">Child elements</span></span>

|<span data-ttu-id="aa395-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa395-113">**Element**</span></span>|<span data-ttu-id="aa395-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa395-114">**Type**</span></span>|<span data-ttu-id="aa395-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa395-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa395-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="aa395-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa395-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="aa395-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aa395-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="aa395-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa395-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="aa395-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aa395-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="aa395-120">Attributes</span></span>

|<span data-ttu-id="aa395-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="aa395-121">**Attribute**</span></span>|<span data-ttu-id="aa395-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="aa395-122">**Type**</span></span>|<span data-ttu-id="aa395-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="aa395-123">**Required**</span></span>|<span data-ttu-id="aa395-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aa395-124">**Description**</span></span>|<span data-ttu-id="aa395-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="aa395-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa395-126">ID</span><span class="sxs-lookup"><span data-stu-id="aa395-126">ID</span></span>  <br/> |<span data-ttu-id="aa395-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="aa395-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aa395-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="aa395-128">required</span></span>  <br/> ||<span data-ttu-id="aa395-129">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="aa395-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aa395-130">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="aa395-130">Ignored</span></span>  <br/> |<span data-ttu-id="aa395-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="aa395-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa395-132">Optional</span><span class="sxs-lookup"><span data-stu-id="aa395-132">optional</span></span>  <br/> ||<span data-ttu-id="aa395-133">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="aa395-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

