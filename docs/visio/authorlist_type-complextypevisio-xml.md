---
title: AuthorList_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394552"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="73555-102">AuthorList_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="73555-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="73555-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="73555-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73555-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="73555-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="73555-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="73555-105">**Schema file**</span></span> <br/> |<span data-ttu-id="73555-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="73555-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="73555-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="73555-107">**Extension base**</span></span> <br/> |<span data-ttu-id="73555-108">Keine</span><span class="sxs-lookup"><span data-stu-id="73555-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73555-109">Definition</span><span class="sxs-lookup"><span data-stu-id="73555-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="73555-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="73555-110">Elements and attributes</span></span>

<span data-ttu-id="73555-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="73555-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="73555-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73555-112">Child elements</span></span>

|<span data-ttu-id="73555-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="73555-113">**Element**</span></span>|<span data-ttu-id="73555-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="73555-114">**Type**</span></span>|<span data-ttu-id="73555-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73555-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73555-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="73555-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="73555-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="73555-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="73555-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="73555-118">Attributes</span></span>

<span data-ttu-id="73555-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="73555-119">None.</span></span>
  

