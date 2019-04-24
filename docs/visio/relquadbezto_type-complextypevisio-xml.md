---
title: RelQuadBezTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 558c7315-5025-484b-446e-333890bc1c3a
ms.openlocfilehash: d584891576967f3e452402667f0adaad5c87843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320167"
---
# <a name="relquadbeztotype-complextype-visio-xml"></a><span data-ttu-id="2c74c-102">RelQuadBezTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2c74c-102">RelQuadBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2c74c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2c74c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c74c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2c74c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2c74c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2c74c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2c74c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2c74c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2c74c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2c74c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2c74c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2c74c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2c74c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2c74c-109">Definition</span></span>

```XML
          <xs:complexType name="RelQuadBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2c74c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2c74c-110">Elements and attributes</span></span>

<span data-ttu-id="2c74c-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2c74c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2c74c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c74c-112">Child elements</span></span>

|<span data-ttu-id="2c74c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c74c-113">**Element**</span></span>|<span data-ttu-id="2c74c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2c74c-114">**Type**</span></span>|<span data-ttu-id="2c74c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c74c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2c74c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2c74c-116">Cell</span></span>](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="2c74c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2c74c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2c74c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c74c-118">Attributes</span></span>

<span data-ttu-id="2c74c-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c74c-119">None.</span></span>
  

