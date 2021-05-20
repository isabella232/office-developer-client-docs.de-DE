---
title: Extensions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7fe070087afab9cdc6eac9e35a230b02ab7d62ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542373"
---
# <a name="extensions_type-complextype-visio-xml"></a><span data-ttu-id="c9efd-102">Extensions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c9efd-102">Extensions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c9efd-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="c9efd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9efd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c9efd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9efd-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c9efd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9efd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9efd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9efd-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="c9efd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9efd-108">Keine</span><span class="sxs-lookup"><span data-stu-id="c9efd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9efd-109">Definition</span><span class="sxs-lookup"><span data-stu-id="c9efd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c9efd-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c9efd-110">Elements and attributes</span></span>

<span data-ttu-id="c9efd-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c9efd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9efd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9efd-112">Child elements</span></span>

|<span data-ttu-id="c9efd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9efd-113">**Element**</span></span>|<span data-ttu-id="c9efd-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c9efd-114">**Type**</span></span>|<span data-ttu-id="c9efd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9efd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9efd-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="c9efd-116">CellDef</span></span> <br/> |[<span data-ttu-id="c9efd-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="c9efd-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="c9efd-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="c9efd-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="c9efd-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="c9efd-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="c9efd-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="c9efd-120">SectionDef</span></span> <br/> |[<span data-ttu-id="c9efd-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="c9efd-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9efd-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9efd-122">Attributes</span></span>

<span data-ttu-id="c9efd-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9efd-123">None.</span></span>
  

