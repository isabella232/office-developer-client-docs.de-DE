---
title: Extensions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351086"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="191d1-102">Extensions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="191d1-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="191d1-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="191d1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="191d1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="191d1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="191d1-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="191d1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="191d1-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="191d1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="191d1-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="191d1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="191d1-108">Keine</span><span class="sxs-lookup"><span data-stu-id="191d1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="191d1-109">Definition</span><span class="sxs-lookup"><span data-stu-id="191d1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="191d1-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="191d1-110">Elements and attributes</span></span>

<span data-ttu-id="191d1-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="191d1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="191d1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="191d1-112">Child elements</span></span>

|<span data-ttu-id="191d1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="191d1-113">**Element**</span></span>|<span data-ttu-id="191d1-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="191d1-114">**Type**</span></span>|<span data-ttu-id="191d1-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="191d1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="191d1-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="191d1-116">CellDef</span></span> <br/> |[<span data-ttu-id="191d1-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="191d1-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="191d1-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="191d1-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="191d1-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="191d1-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="191d1-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="191d1-120">SectionDef</span></span> <br/> |[<span data-ttu-id="191d1-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="191d1-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="191d1-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="191d1-122">Attributes</span></span>

<span data-ttu-id="191d1-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="191d1-123">None.</span></span>
  

