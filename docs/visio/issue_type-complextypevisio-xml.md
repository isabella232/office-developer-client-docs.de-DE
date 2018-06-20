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
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="a1b32-102">Issue_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="a1b32-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a1b32-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a1b32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1b32-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a1b32-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1b32-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a1b32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1b32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1b32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1b32-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a1b32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1b32-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a1b32-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1b32-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a1b32-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a1b32-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a1b32-110">Elements and attributes</span></span>

<span data-ttu-id="a1b32-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="a1b32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1b32-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1b32-112">Child elements</span></span>

|<span data-ttu-id="a1b32-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1b32-113">**Element**</span></span>|<span data-ttu-id="a1b32-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a1b32-114">**Type**</span></span>|<span data-ttu-id="a1b32-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1b32-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1b32-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="a1b32-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1b32-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="a1b32-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1b32-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="a1b32-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1b32-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="a1b32-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a1b32-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="a1b32-120">Attributes</span></span>

|<span data-ttu-id="a1b32-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a1b32-121">**Attribute**</span></span>|<span data-ttu-id="a1b32-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a1b32-122">**Type**</span></span>|<span data-ttu-id="a1b32-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a1b32-123">**Required**</span></span>|<span data-ttu-id="a1b32-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1b32-124">**Description**</span></span>|<span data-ttu-id="a1b32-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a1b32-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a1b32-126">ID</span><span class="sxs-lookup"><span data-stu-id="a1b32-126">ID</span></span>  <br/> |<span data-ttu-id="a1b32-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a1b32-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1b32-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a1b32-128">required</span></span>  <br/> ||<span data-ttu-id="a1b32-129">Werte des Typs Xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a1b32-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a1b32-130">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="a1b32-130">Ignored</span></span>  <br/> |<span data-ttu-id="a1b32-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="a1b32-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1b32-132">Optional</span><span class="sxs-lookup"><span data-stu-id="a1b32-132">optional</span></span>  <br/> ||<span data-ttu-id="a1b32-133">Werte des Typs xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a1b32-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

