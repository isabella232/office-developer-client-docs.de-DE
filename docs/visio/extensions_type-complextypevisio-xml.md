---
title: Extensions_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 670c060cc6f12c664eb615fffb8ec1234891f2b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592136"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="628dc-102">Extensions_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="628dc-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="628dc-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="628dc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="628dc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="628dc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="628dc-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="628dc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="628dc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="628dc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="628dc-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="628dc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="628dc-108">Keine</span><span class="sxs-lookup"><span data-stu-id="628dc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="628dc-109">Definition</span><span class="sxs-lookup"><span data-stu-id="628dc-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="628dc-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="628dc-110">Elements and attributes</span></span>

<span data-ttu-id="628dc-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="628dc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="628dc-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="628dc-112">Child elements</span></span>

|<span data-ttu-id="628dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="628dc-113">**Element**</span></span>|<span data-ttu-id="628dc-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="628dc-114">**Type**</span></span>|<span data-ttu-id="628dc-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="628dc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="628dc-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="628dc-116">CellDef</span></span> <br/> |[<span data-ttu-id="628dc-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="628dc-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="628dc-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="628dc-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="628dc-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="628dc-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="628dc-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="628dc-120">SectionDef</span></span> <br/> |[<span data-ttu-id="628dc-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="628dc-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="628dc-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="628dc-122">Attributes</span></span>

<span data-ttu-id="628dc-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="628dc-123">None.</span></span>
  

