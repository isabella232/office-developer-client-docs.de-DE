---
title: Text_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332305"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="33056-102">Text_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="33056-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="33056-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="33056-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33056-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="33056-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="33056-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="33056-105">**Schema file**</span></span> <br/> |<span data-ttu-id="33056-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="33056-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="33056-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="33056-107">**Extension base**</span></span> <br/> |<span data-ttu-id="33056-108">Keine</span><span class="sxs-lookup"><span data-stu-id="33056-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33056-109">Definition</span><span class="sxs-lookup"><span data-stu-id="33056-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="33056-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="33056-110">Elements and attributes</span></span>

<span data-ttu-id="33056-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="33056-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="33056-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33056-112">Child elements</span></span>

|<span data-ttu-id="33056-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="33056-113">**Element**</span></span>|<span data-ttu-id="33056-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="33056-114">**Type**</span></span>|<span data-ttu-id="33056-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33056-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="33056-116">CP</span><span class="sxs-lookup"><span data-stu-id="33056-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33056-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="33056-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33056-118">fld</span><span class="sxs-lookup"><span data-stu-id="33056-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33056-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="33056-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33056-120">PP</span><span class="sxs-lookup"><span data-stu-id="33056-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33056-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="33056-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="33056-122">TP</span><span class="sxs-lookup"><span data-stu-id="33056-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33056-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="33056-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="33056-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="33056-124">Attributes</span></span>

<span data-ttu-id="33056-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="33056-125">None.</span></span>
  

