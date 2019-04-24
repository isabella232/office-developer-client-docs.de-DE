---
title: IssueTarget_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314924"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="9c70b-102">IssueTarget_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9c70b-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9c70b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9c70b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c70b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c70b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9c70b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9c70b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9c70b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9c70b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9c70b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9c70b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9c70b-108">Keine</span><span class="sxs-lookup"><span data-stu-id="9c70b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c70b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9c70b-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c70b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9c70b-110">Elements and attributes</span></span>

<span data-ttu-id="9c70b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9c70b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9c70b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c70b-112">Child elements</span></span>

<span data-ttu-id="9c70b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c70b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c70b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="9c70b-114">Attributes</span></span>

|<span data-ttu-id="9c70b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9c70b-115">**Attribute**</span></span>|<span data-ttu-id="9c70b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9c70b-116">**Type**</span></span>|<span data-ttu-id="9c70b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9c70b-117">**Required**</span></span>|<span data-ttu-id="9c70b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c70b-118">**Description**</span></span>|<span data-ttu-id="9c70b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9c70b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c70b-120">PageID</span><span class="sxs-lookup"><span data-stu-id="9c70b-120">PageID</span></span>  <br/> |<span data-ttu-id="9c70b-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c70b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c70b-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9c70b-122">required</span></span>  <br/> ||<span data-ttu-id="9c70b-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9c70b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c70b-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="9c70b-124">ShapeID</span></span>  <br/> |<span data-ttu-id="9c70b-125">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c70b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c70b-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9c70b-126">required</span></span>  <br/> ||<span data-ttu-id="9c70b-127">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="9c70b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

