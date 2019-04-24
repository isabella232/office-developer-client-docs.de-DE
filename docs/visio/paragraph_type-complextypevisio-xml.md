---
title: Paragraph_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 8a57a0df516f998e4e815240f1405962e11f848d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338808"
---
# <a name="paragraphtype-complextype-visio-xml"></a><span data-ttu-id="69eaf-102">Paragraph_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="69eaf-102">Paragraph_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="69eaf-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="69eaf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69eaf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69eaf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69eaf-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="69eaf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69eaf-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="69eaf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69eaf-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="69eaf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69eaf-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="69eaf-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69eaf-109">Definition</span><span class="sxs-lookup"><span data-stu-id="69eaf-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="69eaf-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="69eaf-110">Elements and attributes</span></span>

<span data-ttu-id="69eaf-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="69eaf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69eaf-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69eaf-112">Child elements</span></span>

|<span data-ttu-id="69eaf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="69eaf-113">**Element**</span></span>|<span data-ttu-id="69eaf-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="69eaf-114">**Type**</span></span>|<span data-ttu-id="69eaf-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69eaf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69eaf-116">Row</span><span class="sxs-lookup"><span data-stu-id="69eaf-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="69eaf-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="69eaf-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69eaf-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="69eaf-118">Attributes</span></span>

<span data-ttu-id="69eaf-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="69eaf-119">None.</span></span>
  

