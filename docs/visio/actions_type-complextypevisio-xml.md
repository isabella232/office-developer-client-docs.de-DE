---
title: Actions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 384b948c61f3b618d108db090721ea6768d69372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538410"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="cc186-102">Actions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cc186-102">Actions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cc186-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="cc186-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc186-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc186-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc186-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="cc186-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc186-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cc186-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc186-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="cc186-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc186-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="cc186-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc186-109">Definition</span><span class="sxs-lookup"><span data-stu-id="cc186-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc186-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="cc186-110">Elements and attributes</span></span>

<span data-ttu-id="cc186-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="cc186-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc186-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc186-112">Child elements</span></span>

|<span data-ttu-id="cc186-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc186-113">**Element**</span></span>|<span data-ttu-id="cc186-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="cc186-114">**Type**</span></span>|<span data-ttu-id="cc186-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc186-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc186-116">Row</span><span class="sxs-lookup"><span data-stu-id="cc186-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="cc186-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="cc186-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cc186-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc186-118">Attributes</span></span>

<span data-ttu-id="cc186-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc186-119">None.</span></span>
  

