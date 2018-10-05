---
title: Text_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384787"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="d5af4-102">Text_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="d5af4-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d5af4-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d5af4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5af4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5af4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5af4-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d5af4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5af4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5af4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5af4-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d5af4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5af4-108">Keine</span><span class="sxs-lookup"><span data-stu-id="d5af4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5af4-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d5af4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5af4-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d5af4-110">Elements and attributes</span></span>

<span data-ttu-id="d5af4-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d5af4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5af4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5af4-112">Child elements</span></span>

|<span data-ttu-id="d5af4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5af4-113">**Element**</span></span>|<span data-ttu-id="d5af4-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d5af4-114">**Type**</span></span>|<span data-ttu-id="d5af4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5af4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5af4-116">CP-Werts</span><span class="sxs-lookup"><span data-stu-id="d5af4-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5af4-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="d5af4-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5af4-118">fld</span><span class="sxs-lookup"><span data-stu-id="d5af4-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5af4-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="d5af4-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5af4-120">PS</span><span class="sxs-lookup"><span data-stu-id="d5af4-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5af4-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="d5af4-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5af4-122">TP</span><span class="sxs-lookup"><span data-stu-id="d5af4-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5af4-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="d5af4-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d5af4-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5af4-124">Attributes</span></span>

<span data-ttu-id="d5af4-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5af4-125">None.</span></span>
  

