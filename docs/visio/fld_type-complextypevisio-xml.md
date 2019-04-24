---
title: fld_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346207"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="00033-102">fld_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="00033-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="00033-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="00033-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00033-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="00033-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="00033-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="00033-105">**Schema file**</span></span> <br/> |<span data-ttu-id="00033-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="00033-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="00033-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="00033-107">**Extension base**</span></span> <br/> |<span data-ttu-id="00033-108">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00033-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00033-109">Definition</span><span class="sxs-lookup"><span data-stu-id="00033-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="00033-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="00033-110">Elements and attributes</span></span>

<span data-ttu-id="00033-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="00033-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="00033-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00033-112">Child elements</span></span>

<span data-ttu-id="00033-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="00033-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00033-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="00033-114">Attributes</span></span>

|<span data-ttu-id="00033-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="00033-115">**Attribute**</span></span>|<span data-ttu-id="00033-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="00033-116">**Type**</span></span>|<span data-ttu-id="00033-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="00033-117">**Required**</span></span>|<span data-ttu-id="00033-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00033-118">**Description**</span></span>|<span data-ttu-id="00033-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="00033-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="00033-120">IX</span><span class="sxs-lookup"><span data-stu-id="00033-120">IX</span></span>  <br/> |<span data-ttu-id="00033-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="00033-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="00033-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00033-122">required</span></span>  <br/> ||<span data-ttu-id="00033-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="00033-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

