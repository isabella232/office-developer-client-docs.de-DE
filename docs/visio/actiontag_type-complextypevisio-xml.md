---
title: ActionTag_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: a30290ee9dbb86c7af75820bd767bb95ce4add21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283058"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="34f54-102">ActionTag_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="34f54-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="34f54-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="34f54-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34f54-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34f54-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="34f54-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="34f54-105">**Schema file**</span></span> <br/> |<span data-ttu-id="34f54-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="34f54-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="34f54-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="34f54-107">**Extension base**</span></span> <br/> |<span data-ttu-id="34f54-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="34f54-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34f54-109">Definition</span><span class="sxs-lookup"><span data-stu-id="34f54-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="34f54-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="34f54-110">Elements and attributes</span></span>

<span data-ttu-id="34f54-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="34f54-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="34f54-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34f54-112">Child elements</span></span>

|<span data-ttu-id="34f54-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="34f54-113">**Element**</span></span>|<span data-ttu-id="34f54-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="34f54-114">**Type**</span></span>|<span data-ttu-id="34f54-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34f54-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34f54-116">Row</span><span class="sxs-lookup"><span data-stu-id="34f54-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="34f54-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="34f54-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="34f54-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="34f54-118">Attributes</span></span>

<span data-ttu-id="34f54-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="34f54-119">None.</span></span>
  

