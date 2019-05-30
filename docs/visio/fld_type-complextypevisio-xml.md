---
title: fld_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539600"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="bc9d5-102">fld_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bc9d5-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bc9d5-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="bc9d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc9d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bc9d5-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bc9d5-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="bc9d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bc9d5-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bc9d5-108">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bc9d5-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bc9d5-109">Definition</span><span class="sxs-lookup"><span data-stu-id="bc9d5-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bc9d5-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bc9d5-110">Elements and attributes</span></span>

<span data-ttu-id="bc9d5-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="bc9d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bc9d5-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc9d5-112">Child elements</span></span>

<span data-ttu-id="bc9d5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bc9d5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc9d5-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="bc9d5-114">Attributes</span></span>

|<span data-ttu-id="bc9d5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-115">**Attribute**</span></span>|<span data-ttu-id="bc9d5-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-116">**Type**</span></span>|<span data-ttu-id="bc9d5-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-117">**Required**</span></span>|<span data-ttu-id="bc9d5-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-118">**Description**</span></span>|<span data-ttu-id="bc9d5-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="bc9d5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bc9d5-120">IX</span><span class="sxs-lookup"><span data-stu-id="bc9d5-120">IX</span></span>  <br/> |<span data-ttu-id="bc9d5-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bc9d5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bc9d5-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="bc9d5-122">required</span></span>  <br/> ||<span data-ttu-id="bc9d5-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="bc9d5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

