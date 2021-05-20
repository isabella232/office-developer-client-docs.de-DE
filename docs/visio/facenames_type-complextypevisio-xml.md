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
# <a name="facenames_type-complextype-visio-xml"></a><span data-ttu-id="ac460-102">FaceNames_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ac460-102">FaceNames_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ac460-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ac460-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac460-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac460-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ac460-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ac460-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ac460-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ac460-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ac460-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ac460-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ac460-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ac460-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac460-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ac460-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ac460-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ac460-110">Elements and attributes</span></span>

<span data-ttu-id="ac460-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ac460-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ac460-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac460-112">Child elements</span></span>

|<span data-ttu-id="ac460-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac460-113">**Element**</span></span>|<span data-ttu-id="ac460-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ac460-114">**Type**</span></span>|<span data-ttu-id="ac460-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac460-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac460-116">FaceName</span><span class="sxs-lookup"><span data-stu-id="ac460-116">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ac460-117">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="ac460-117">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ac460-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac460-118">Attributes</span></span>

<span data-ttu-id="ac460-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac460-119">None.</span></span>
  

