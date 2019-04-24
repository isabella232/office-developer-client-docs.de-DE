---
title: DataColumns_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344597"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="92fcb-102">DataColumns_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="92fcb-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="92fcb-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="92fcb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92fcb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92fcb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92fcb-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="92fcb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92fcb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="92fcb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92fcb-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="92fcb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92fcb-108">Keine</span><span class="sxs-lookup"><span data-stu-id="92fcb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92fcb-109">Definition</span><span class="sxs-lookup"><span data-stu-id="92fcb-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92fcb-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="92fcb-110">Elements and attributes</span></span>

<span data-ttu-id="92fcb-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="92fcb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92fcb-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92fcb-112">Child elements</span></span>

|<span data-ttu-id="92fcb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="92fcb-113">**Element**</span></span>|<span data-ttu-id="92fcb-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92fcb-114">**Type**</span></span>|<span data-ttu-id="92fcb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92fcb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92fcb-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="92fcb-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92fcb-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="92fcb-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="92fcb-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="92fcb-118">Attributes</span></span>

|<span data-ttu-id="92fcb-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92fcb-119">**Attribute**</span></span>|<span data-ttu-id="92fcb-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="92fcb-120">**Type**</span></span>|<span data-ttu-id="92fcb-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="92fcb-121">**Required**</span></span>|<span data-ttu-id="92fcb-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92fcb-122">**Description**</span></span>|<span data-ttu-id="92fcb-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="92fcb-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92fcb-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="92fcb-124">SortAsc</span></span>  <br/> |<span data-ttu-id="92fcb-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="92fcb-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="92fcb-126">Optional</span><span class="sxs-lookup"><span data-stu-id="92fcb-126">optional</span></span>  <br/> ||<span data-ttu-id="92fcb-127">Werte des XSD: Boolean-Typs.</span><span class="sxs-lookup"><span data-stu-id="92fcb-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="92fcb-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="92fcb-128">SortColumn</span></span>  <br/> |<span data-ttu-id="92fcb-129">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="92fcb-129">xsd:string</span></span>  <br/> |<span data-ttu-id="92fcb-130">Optional</span><span class="sxs-lookup"><span data-stu-id="92fcb-130">optional</span></span>  <br/> ||<span data-ttu-id="92fcb-131">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="92fcb-131">Values of the xsd:string type.</span></span>  <br/> |
   

