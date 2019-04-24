---
title: FaceNames_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 6f9cd84dffc22f4211a8445a2d493ef7d4f4a4f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322589"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="2830d-102">FaceNames_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2830d-102">FaceNames_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2830d-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="2830d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2830d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2830d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2830d-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="2830d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2830d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2830d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2830d-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="2830d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2830d-108">Keine</span><span class="sxs-lookup"><span data-stu-id="2830d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2830d-109">Definition</span><span class="sxs-lookup"><span data-stu-id="2830d-109">Definition</span></span>

```XML
          <xs:complexType name="FaceNames_Type">
          
          <xs:sequence>
    <xs:element name="FaceName"  type="FaceName_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2830d-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="2830d-110">Elements and attributes</span></span>

<span data-ttu-id="2830d-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="2830d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2830d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2830d-112">Child elements</span></span>

|<span data-ttu-id="2830d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2830d-113">**Element**</span></span>|<span data-ttu-id="2830d-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="2830d-114">**Type**</span></span>|<span data-ttu-id="2830d-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2830d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2830d-116">FaceName</span><span class="sxs-lookup"><span data-stu-id="2830d-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2830d-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="2830d-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2830d-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="2830d-118">Attributes</span></span>

<span data-ttu-id="2830d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="2830d-119">None.</span></span>
  

