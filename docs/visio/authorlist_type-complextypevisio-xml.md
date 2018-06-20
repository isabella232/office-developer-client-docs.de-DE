---
title: AuthorList_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: e4cee87a5060580e8b7f1efc7970091d56fd310f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796394"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="46024-102">AuthorList_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="46024-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="46024-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="46024-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46024-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="46024-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="46024-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="46024-105">**Schema file**</span></span> <br/> |<span data-ttu-id="46024-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="46024-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="46024-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="46024-107">**Extension base**</span></span> <br/> |<span data-ttu-id="46024-108">Keine</span><span class="sxs-lookup"><span data-stu-id="46024-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46024-109">Definition</span><span class="sxs-lookup"><span data-stu-id="46024-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46024-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="46024-110">Elements and attributes</span></span>

<span data-ttu-id="46024-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="46024-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="46024-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46024-112">Child elements</span></span>

|<span data-ttu-id="46024-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="46024-113">**Element**</span></span>|<span data-ttu-id="46024-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="46024-114">**Type**</span></span>|<span data-ttu-id="46024-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46024-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46024-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="46024-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46024-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="46024-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="46024-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="46024-118">Attributes</span></span>

<span data-ttu-id="46024-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="46024-119">None.</span></span>
  

