---
title: Text_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: 3309184c47eaf6c6a8cb20d7c6485c21c5ec8c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798231"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="0d51c-102">Text_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="0d51c-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d51c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0d51c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d51c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d51c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d51c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0d51c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d51c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0d51c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d51c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0d51c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d51c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="0d51c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d51c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="0d51c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0d51c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0d51c-110">Elements and attributes</span></span>

<span data-ttu-id="0d51c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0d51c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d51c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d51c-112">Child elements</span></span>

|<span data-ttu-id="0d51c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d51c-113">**Element**</span></span>|<span data-ttu-id="0d51c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0d51c-114">**Type**</span></span>|<span data-ttu-id="0d51c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d51c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d51c-116">CP-Werts</span><span class="sxs-lookup"><span data-stu-id="0d51c-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d51c-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="0d51c-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0d51c-118">fld</span><span class="sxs-lookup"><span data-stu-id="0d51c-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d51c-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="0d51c-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0d51c-120">PS</span><span class="sxs-lookup"><span data-stu-id="0d51c-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d51c-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="0d51c-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0d51c-122">TP</span><span class="sxs-lookup"><span data-stu-id="0d51c-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d51c-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="0d51c-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d51c-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d51c-124">Attributes</span></span>

<span data-ttu-id="0d51c-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d51c-125">None.</span></span>
  

