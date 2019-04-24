---
title: PageSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 45e3dec8dc97fd3467195102a42227b844f07a98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334650"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="a5b5b-102">PageSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a5b5b-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a5b5b-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a5b5b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5b5b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a5b5b-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a5b5b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a5b5b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a5b5b-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a5b5b-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a5b5b-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a5b5b-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a5b5b-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a5b5b-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a5b5b-110">Elements and attributes</span></span>

<span data-ttu-id="a5b5b-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a5b5b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5b5b-112">Child elements</span></span>

<span data-ttu-id="a5b5b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5b5b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5b5b-114">Attributes</span></span>

|<span data-ttu-id="a5b5b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-115">**Attribute**</span></span>|<span data-ttu-id="a5b5b-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-116">**Type**</span></span>|<span data-ttu-id="a5b5b-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-117">**Required**</span></span>|<span data-ttu-id="a5b5b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-118">**Description**</span></span>|<span data-ttu-id="a5b5b-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a5b5b-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="a5b5b-120">UniqueID</span></span>  <br/> |<span data-ttu-id="a5b5b-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a5b5b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a5b5b-122">Optional</span><span class="sxs-lookup"><span data-stu-id="a5b5b-122">optional</span></span>  <br/> ||<span data-ttu-id="a5b5b-123">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-123">Values of the xsd:string type.</span></span>  <br/> |
   

