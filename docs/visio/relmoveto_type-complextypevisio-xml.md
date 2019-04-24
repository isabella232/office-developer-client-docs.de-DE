---
title: RelMoveTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3759d7cc-061b-0c0b-c372-b7d60effbfd0
ms.openlocfilehash: ff1a822b749fcddb2f3712a5eb82f12aabec0144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320097"
---
# <a name="relmovetotype-complextype-visio-xml"></a><span data-ttu-id="ef7f4-102">RelMoveTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ef7f4-102">RelMoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ef7f4-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ef7f4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef7f4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ef7f4-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ef7f4-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ef7f4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ef7f4-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ef7f4-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="ef7f4-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef7f4-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ef7f4-109">Definition</span></span>

```XML
          <xs:complexType name="RelMoveTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef7f4-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ef7f4-110">Elements and attributes</span></span>

<span data-ttu-id="ef7f4-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ef7f4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ef7f4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef7f4-112">Child elements</span></span>

|<span data-ttu-id="ef7f4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-113">**Element**</span></span>|<span data-ttu-id="ef7f4-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-114">**Type**</span></span>|<span data-ttu-id="ef7f4-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef7f4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef7f4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ef7f4-116">Cell</span></span>](cell-element-relmoveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="ef7f4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ef7f4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ef7f4-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef7f4-118">Attributes</span></span>

<span data-ttu-id="ef7f4-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef7f4-119">None.</span></span>
  

