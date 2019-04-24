---
title: ActionTagRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 8caef77494efa99df8f681deb1268dfee95f03cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346557"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="5f466-102">ActionTagRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5f466-102">ActionTagRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5f466-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5f466-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f466-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5f466-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5f466-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5f466-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5f466-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="5f466-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5f466-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5f466-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5f466-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="5f466-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5f466-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5f466-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5f466-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5f466-110">Elements and attributes</span></span>

<span data-ttu-id="5f466-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="5f466-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5f466-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f466-112">Child elements</span></span>

|<span data-ttu-id="5f466-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f466-113">**Element**</span></span>|<span data-ttu-id="5f466-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5f466-114">**Type**</span></span>|<span data-ttu-id="5f466-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f466-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5f466-116">Cell</span><span class="sxs-lookup"><span data-stu-id="5f466-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5f466-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5f466-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5f466-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f466-118">Attributes</span></span>

<span data-ttu-id="5f466-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f466-119">None.</span></span>
  

