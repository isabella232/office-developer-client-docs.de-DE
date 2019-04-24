---
title: Field_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c346fb8d-f247-4a14-19cd-9368ec86ce3f
ms.openlocfilehash: d711209ce1663f657b9a22fc6d4837ab51909647
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322540"
---
# <a name="fieldtype-complextype-visio-xml"></a><span data-ttu-id="98834-102">Field_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="98834-102">Field_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="98834-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="98834-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98834-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="98834-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="98834-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="98834-105">**Schema file**</span></span> <br/> |<span data-ttu-id="98834-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="98834-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="98834-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="98834-107">**Extension base**</span></span> <br/> |<span data-ttu-id="98834-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="98834-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98834-109">Definition</span><span class="sxs-lookup"><span data-stu-id="98834-109">Definition</span></span>

```XML
          <xs:complexType name="Field_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FieldRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="98834-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="98834-110">Elements and attributes</span></span>

<span data-ttu-id="98834-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="98834-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="98834-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="98834-112">Child elements</span></span>

|<span data-ttu-id="98834-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="98834-113">**Element**</span></span>|<span data-ttu-id="98834-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="98834-114">**Type**</span></span>|<span data-ttu-id="98834-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98834-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98834-116">Row</span><span class="sxs-lookup"><span data-stu-id="98834-116">Row</span></span>](row-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="98834-117">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="98834-117">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="98834-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="98834-118">Attributes</span></span>

<span data-ttu-id="98834-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="98834-119">None.</span></span>
  

