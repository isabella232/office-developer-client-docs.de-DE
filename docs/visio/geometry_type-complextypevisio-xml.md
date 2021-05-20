---
title: Geometry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 1b16a32462f997ab80b0b6ef64df8eb202740c47
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542289"
---
# <a name="geometry_type-complextype-visio-xml"></a><span data-ttu-id="d6556-102">Geometry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d6556-102">Geometry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d6556-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d6556-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6556-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6556-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d6556-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d6556-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d6556-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d6556-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d6556-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d6556-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d6556-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d6556-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6556-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d6556-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6556-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d6556-110">Elements and attributes</span></span>

<span data-ttu-id="d6556-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d6556-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d6556-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6556-112">Child elements</span></span>

|<span data-ttu-id="d6556-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6556-113">**Element**</span></span>|<span data-ttu-id="d6556-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d6556-114">**Type**</span></span>|<span data-ttu-id="d6556-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6556-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6556-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d6556-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d6556-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d6556-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d6556-118">Zeile</span><span class="sxs-lookup"><span data-stu-id="d6556-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="d6556-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="d6556-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d6556-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6556-120">Attributes</span></span>

<span data-ttu-id="d6556-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6556-121">None.</span></span>
  

