---
title: FooterMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346046"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="a3b16-102">FooterMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a3b16-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a3b16-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="a3b16-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3b16-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a3b16-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a3b16-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a3b16-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a3b16-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a3b16-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a3b16-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="a3b16-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a3b16-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a3b16-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3b16-109">Definition</span><span class="sxs-lookup"><span data-stu-id="a3b16-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3b16-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a3b16-110">Elements and attributes</span></span>

<span data-ttu-id="a3b16-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a3b16-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a3b16-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a3b16-112">Child elements</span></span>

<span data-ttu-id="a3b16-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a3b16-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3b16-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a3b16-114">Attributes</span></span>

|<span data-ttu-id="a3b16-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a3b16-115">**Attribute**</span></span>|<span data-ttu-id="a3b16-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a3b16-116">**Type**</span></span>|<span data-ttu-id="a3b16-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a3b16-117">**Required**</span></span>|<span data-ttu-id="a3b16-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3b16-118">**Description**</span></span>|<span data-ttu-id="a3b16-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a3b16-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3b16-120">Unit</span><span class="sxs-lookup"><span data-stu-id="a3b16-120">Unit</span></span>  <br/> |<span data-ttu-id="a3b16-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3b16-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a3b16-122">Optional</span><span class="sxs-lookup"><span data-stu-id="a3b16-122">optional</span></span>  <br/> ||<span data-ttu-id="a3b16-123">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="a3b16-123">Values of the xsd:string type.</span></span>  <br/> |
   

