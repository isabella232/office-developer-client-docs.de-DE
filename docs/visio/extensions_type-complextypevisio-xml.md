---
title: Extensions_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398136"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="c1d89-102">Extensions_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="c1d89-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c1d89-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c1d89-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1d89-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1d89-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c1d89-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c1d89-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c1d89-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c1d89-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c1d89-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c1d89-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c1d89-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c1d89-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1d89-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c1d89-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c1d89-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c1d89-110">Elements and attributes</span></span>

<span data-ttu-id="c1d89-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c1d89-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c1d89-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1d89-112">Child elements</span></span>

|<span data-ttu-id="c1d89-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1d89-113">**Element**</span></span>|<span data-ttu-id="c1d89-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c1d89-114">**Type**</span></span>|<span data-ttu-id="c1d89-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1d89-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1d89-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="c1d89-116">CellDef</span></span> <br/> |[<span data-ttu-id="c1d89-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="c1d89-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="c1d89-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="c1d89-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="c1d89-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="c1d89-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="c1d89-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="c1d89-120">SectionDef</span></span> <br/> |[<span data-ttu-id="c1d89-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="c1d89-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c1d89-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1d89-122">Attributes</span></span>

<span data-ttu-id="c1d89-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1d89-123">None.</span></span>
  

