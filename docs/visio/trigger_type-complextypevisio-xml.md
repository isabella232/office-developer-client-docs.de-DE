---
title: Trigger_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280857"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="43a45-102">Trigger_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="43a45-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43a45-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="43a45-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43a45-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43a45-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43a45-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="43a45-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43a45-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="43a45-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43a45-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="43a45-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43a45-108">Keine</span><span class="sxs-lookup"><span data-stu-id="43a45-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43a45-109">Definition</span><span class="sxs-lookup"><span data-stu-id="43a45-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43a45-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="43a45-110">Elements and attributes</span></span>

<span data-ttu-id="43a45-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="43a45-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43a45-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43a45-112">Child elements</span></span>

|<span data-ttu-id="43a45-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="43a45-113">**Element**</span></span>|<span data-ttu-id="43a45-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="43a45-114">**Type**</span></span>|<span data-ttu-id="43a45-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43a45-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43a45-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="43a45-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43a45-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="43a45-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="43a45-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="43a45-118">Attributes</span></span>

|<span data-ttu-id="43a45-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="43a45-119">**Attribute**</span></span>|<span data-ttu-id="43a45-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="43a45-120">**Type**</span></span>|<span data-ttu-id="43a45-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="43a45-121">**Required**</span></span>|<span data-ttu-id="43a45-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43a45-122">**Description**</span></span>|<span data-ttu-id="43a45-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="43a45-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43a45-124">N</span><span class="sxs-lookup"><span data-stu-id="43a45-124">N</span></span>  <br/> |<span data-ttu-id="43a45-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="43a45-125">xsd:string</span></span>  <br/> |<span data-ttu-id="43a45-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="43a45-126">required</span></span>  <br/> ||<span data-ttu-id="43a45-127">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="43a45-127">Values of the xsd:string type.</span></span>  <br/> |
   

