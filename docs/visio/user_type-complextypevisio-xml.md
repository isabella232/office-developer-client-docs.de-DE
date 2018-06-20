---
title: User_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d3970d90-6beb-1f59-256f-ace6a9865b59
ms.openlocfilehash: 855a8b3908cb66c12641b1f364208f698b5a97bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798383"
---
# <a name="usertype-complextype-visio-xml"></a><span data-ttu-id="fc4b8-102">User_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="fc4b8-102">User_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fc4b8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="fc4b8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc4b8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fc4b8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fc4b8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fc4b8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fc4b8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fc4b8-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="fc4b8-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc4b8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="fc4b8-109">Definition</span></span>

```XML
          <xs:complexType name="User_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="UserRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc4b8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="fc4b8-110">Elements and attributes</span></span>

<span data-ttu-id="fc4b8-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fc4b8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc4b8-112">Child elements</span></span>

|<span data-ttu-id="fc4b8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-113">**Element**</span></span>|<span data-ttu-id="fc4b8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-114">**Type**</span></span>|<span data-ttu-id="fc4b8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc4b8-116">Row</span><span class="sxs-lookup"><span data-stu-id="fc4b8-116">Row</span></span>](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fc4b8-117">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="fc4b8-117">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fc4b8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="fc4b8-118">Attributes</span></span>

<span data-ttu-id="fc4b8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-119">None.</span></span>
  

