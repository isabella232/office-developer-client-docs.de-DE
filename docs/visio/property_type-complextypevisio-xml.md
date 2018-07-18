---
title: Property_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ed0cd01a47a1bdd3df77fdd1210f196ec20670b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797735"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="9a2a8-102">Property_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="9a2a8-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9a2a8-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9a2a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a2a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a2a8-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a2a8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a2a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a2a8-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a2a8-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="9a2a8-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a2a8-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9a2a8-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a2a8-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9a2a8-110">Elements and attributes</span></span>

<span data-ttu-id="9a2a8-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a2a8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a2a8-112">Child elements</span></span>

|<span data-ttu-id="9a2a8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-113">**Element**</span></span>|<span data-ttu-id="9a2a8-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-114">**Type**</span></span>|<span data-ttu-id="9a2a8-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9a2a8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a2a8-116">Row</span><span class="sxs-lookup"><span data-stu-id="9a2a8-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9a2a8-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="9a2a8-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9a2a8-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a2a8-118">Attributes</span></span>

<span data-ttu-id="9a2a8-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a2a8-119">None.</span></span>
  

