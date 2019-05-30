---
title: FaceNames_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 234bbe07-004e-0604-144c-376d7b06994b
ms.openlocfilehash: 70ca3c5717ef6f85899a9be2ab4299dcefbd8fa0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542422"
---
# <a name="facenamestype-complextype-visio-xml"></a><span data-ttu-id="21784-102">FaceNames_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="21784-102">FaceNames_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="21784-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="21784-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21784-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21784-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="21784-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="21784-105">**Schema file**</span></span> <br/> |<span data-ttu-id="21784-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="21784-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="21784-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="21784-107">**Extension base**</span></span> <br/> |<span data-ttu-id="21784-108">Keine</span><span class="sxs-lookup"><span data-stu-id="21784-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21784-109">Definition</span><span class="sxs-lookup"><span data-stu-id="21784-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="21784-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="21784-110">Elements and attributes</span></span>

<span data-ttu-id="21784-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="21784-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="21784-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21784-112">Child elements</span></span>

|<span data-ttu-id="21784-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="21784-113">**Element**</span></span>|<span data-ttu-id="21784-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="21784-114">**Type**</span></span>|<span data-ttu-id="21784-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21784-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21784-116">FaceName</span><span class="sxs-lookup"><span data-stu-id="21784-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21784-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="21784-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="21784-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="21784-118">Attributes</span></span>

<span data-ttu-id="21784-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="21784-119">None.</span></span>
  

