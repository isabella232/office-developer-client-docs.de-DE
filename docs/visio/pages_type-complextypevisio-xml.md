---
title: Pages_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400159"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="ac0ab-102">Pages_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="ac0ab-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ac0ab-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ac0ab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac0ab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ac0ab-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ac0ab-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ac0ab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ac0ab-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ac0ab-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ac0ab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac0ab-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ac0ab-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac0ab-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ac0ab-110">Elements and attributes</span></span>

<span data-ttu-id="ac0ab-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="ac0ab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ac0ab-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac0ab-112">Child elements</span></span>

|<span data-ttu-id="ac0ab-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-113">**Element**</span></span>|<span data-ttu-id="ac0ab-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-114">**Type**</span></span>|<span data-ttu-id="ac0ab-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac0ab-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac0ab-116">Page</span><span class="sxs-lookup"><span data-stu-id="ac0ab-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ac0ab-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="ac0ab-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ac0ab-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac0ab-118">Attributes</span></span>

<span data-ttu-id="ac0ab-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac0ab-119">None.</span></span>
  

