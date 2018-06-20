---
title: CommentList_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 640ba8825ffdfaa92c7a7ce43fb6bfb92e19ce12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796661"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="65ee8-102">CommentList_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="65ee8-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="65ee8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="65ee8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65ee8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65ee8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65ee8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="65ee8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65ee8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65ee8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65ee8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="65ee8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65ee8-108">Keine</span><span class="sxs-lookup"><span data-stu-id="65ee8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65ee8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="65ee8-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65ee8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="65ee8-110">Elements and attributes</span></span>

<span data-ttu-id="65ee8-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="65ee8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65ee8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65ee8-112">Child elements</span></span>

|<span data-ttu-id="65ee8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="65ee8-113">**Element**</span></span>|<span data-ttu-id="65ee8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="65ee8-114">**Type**</span></span>|<span data-ttu-id="65ee8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65ee8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65ee8-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="65ee8-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65ee8-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="65ee8-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="65ee8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="65ee8-118">Attributes</span></span>

<span data-ttu-id="65ee8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="65ee8-119">None.</span></span>
  

