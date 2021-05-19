---
title: ScratchRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: c2fec0107bba66809536a1cf8bf43fb616a9ef81
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539026"
---
# <a name="scratchrow_type-complextype-visio-xml"></a><span data-ttu-id="9fe20-102">ScratchRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9fe20-102">ScratchRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9fe20-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="9fe20-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fe20-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9fe20-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9fe20-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9fe20-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9fe20-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9fe20-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9fe20-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="9fe20-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9fe20-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="9fe20-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fe20-109">Definition</span><span class="sxs-lookup"><span data-stu-id="9fe20-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="9fe20-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9fe20-110">Elements and attributes</span></span>

<span data-ttu-id="9fe20-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="9fe20-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9fe20-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fe20-112">Child elements</span></span>

|<span data-ttu-id="9fe20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fe20-113">**Element**</span></span>|<span data-ttu-id="9fe20-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9fe20-114">**Type**</span></span>|<span data-ttu-id="9fe20-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fe20-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fe20-116">Cell</span><span class="sxs-lookup"><span data-stu-id="9fe20-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9fe20-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9fe20-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9fe20-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fe20-118">Attributes</span></span>

<span data-ttu-id="9fe20-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fe20-119">None.</span></span>
  

