---
title: RowKeyValue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541722"
---
# <a name="rowkeyvalue_type-complextype-visio-xml"></a><span data-ttu-id="ba371-102">RowKeyValue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ba371-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ba371-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="ba371-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba371-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba371-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ba371-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="ba371-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ba371-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ba371-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ba371-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="ba371-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ba371-108">Keine</span><span class="sxs-lookup"><span data-stu-id="ba371-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba371-109">Definition</span><span class="sxs-lookup"><span data-stu-id="ba371-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba371-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="ba371-110">Elements and attributes</span></span>

<span data-ttu-id="ba371-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="ba371-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ba371-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba371-112">Child elements</span></span>

<span data-ttu-id="ba371-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba371-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba371-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba371-114">Attributes</span></span>

|<span data-ttu-id="ba371-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ba371-115">**Attribute**</span></span>|<span data-ttu-id="ba371-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="ba371-116">**Type**</span></span>|<span data-ttu-id="ba371-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ba371-117">**Required**</span></span>|<span data-ttu-id="ba371-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba371-118">**Description**</span></span>|<span data-ttu-id="ba371-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="ba371-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ba371-120">RowID</span><span class="sxs-lookup"><span data-stu-id="ba371-120">RowID</span></span>  <br/> |<span data-ttu-id="ba371-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ba371-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ba371-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ba371-122">required</span></span>  <br/> ||<span data-ttu-id="ba371-123">Werte des xsd:unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba371-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ba371-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ba371-124">Value</span></span>  <br/> |<span data-ttu-id="ba371-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ba371-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ba371-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="ba371-126">required</span></span>  <br/> ||<span data-ttu-id="ba371-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="ba371-127">Values of the xsd:string type.</span></span>  <br/> |
   

