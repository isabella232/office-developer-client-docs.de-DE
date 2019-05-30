---
title: CommentList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542051"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="105e8-102">CommentList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="105e8-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="105e8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="105e8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="105e8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="105e8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="105e8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="105e8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="105e8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="105e8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="105e8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="105e8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="105e8-108">Keine</span><span class="sxs-lookup"><span data-stu-id="105e8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="105e8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="105e8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="105e8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="105e8-110">Elements and attributes</span></span>

<span data-ttu-id="105e8-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="105e8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="105e8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="105e8-112">Child elements</span></span>

|<span data-ttu-id="105e8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="105e8-113">**Element**</span></span>|<span data-ttu-id="105e8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="105e8-114">**Type**</span></span>|<span data-ttu-id="105e8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="105e8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="105e8-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="105e8-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="105e8-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="105e8-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="105e8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="105e8-118">Attributes</span></span>

<span data-ttu-id="105e8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="105e8-119">None.</span></span>
  

