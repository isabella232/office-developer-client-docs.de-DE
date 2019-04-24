---
title: HeaderMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330051"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="1b235-102">HeaderMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1b235-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1b235-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="1b235-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b235-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b235-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b235-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1b235-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b235-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1b235-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b235-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="1b235-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b235-108">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="1b235-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b235-109">Definition</span><span class="sxs-lookup"><span data-stu-id="1b235-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b235-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1b235-110">Elements and attributes</span></span>

<span data-ttu-id="1b235-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1b235-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b235-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b235-112">Child elements</span></span>

<span data-ttu-id="1b235-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b235-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b235-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b235-114">Attributes</span></span>

|<span data-ttu-id="1b235-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1b235-115">**Attribute**</span></span>|<span data-ttu-id="1b235-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1b235-116">**Type**</span></span>|<span data-ttu-id="1b235-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1b235-117">**Required**</span></span>|<span data-ttu-id="1b235-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b235-118">**Description**</span></span>|<span data-ttu-id="1b235-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1b235-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b235-120">Unit</span><span class="sxs-lookup"><span data-stu-id="1b235-120">Unit</span></span>  <br/> |<span data-ttu-id="1b235-121">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1b235-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1b235-122">Optional</span><span class="sxs-lookup"><span data-stu-id="1b235-122">optional</span></span>  <br/> ||<span data-ttu-id="1b235-123">Werte des XSD: String-Typs.</span><span class="sxs-lookup"><span data-stu-id="1b235-123">Values of the xsd:string type.</span></span>  <br/> |
   

