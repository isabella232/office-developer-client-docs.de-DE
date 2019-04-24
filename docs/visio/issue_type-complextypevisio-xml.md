---
title: Issue_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339501"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="1bfe0-102">Issue_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1bfe0-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1bfe0-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1bfe0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bfe0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1bfe0-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1bfe0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1bfe0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1bfe0-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1bfe0-108">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfe0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1bfe0-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1bfe0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1bfe0-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfe0-110">Elements and attributes</span></span>

<span data-ttu-id="1bfe0-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1bfe0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1bfe0-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfe0-112">Child elements</span></span>

|<span data-ttu-id="1bfe0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-113">**Element**</span></span>|<span data-ttu-id="1bfe0-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-114">**Type**</span></span>|<span data-ttu-id="1bfe0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1bfe0-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="1bfe0-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1bfe0-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="1bfe0-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1bfe0-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="1bfe0-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1bfe0-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="1bfe0-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1bfe0-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfe0-120">Attributes</span></span>

|<span data-ttu-id="1bfe0-121">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-121">**Attribute**</span></span>|<span data-ttu-id="1bfe0-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-122">**Type**</span></span>|<span data-ttu-id="1bfe0-123">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-123">**Required**</span></span>|<span data-ttu-id="1bfe0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-124">**Description**</span></span>|<span data-ttu-id="1bfe0-125">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1bfe0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1bfe0-126">ID</span><span class="sxs-lookup"><span data-stu-id="1bfe0-126">ID</span></span>  <br/> |<span data-ttu-id="1bfe0-127">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1bfe0-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1bfe0-128">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1bfe0-128">required</span></span>  <br/> ||<span data-ttu-id="1bfe0-129">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="1bfe0-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1bfe0-130">Ignoriert</span><span class="sxs-lookup"><span data-stu-id="1bfe0-130">Ignored</span></span>  <br/> |<span data-ttu-id="1bfe0-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="1bfe0-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1bfe0-132">Optional</span><span class="sxs-lookup"><span data-stu-id="1bfe0-132">optional</span></span>  <br/> ||<span data-ttu-id="1bfe0-133">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="1bfe0-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

