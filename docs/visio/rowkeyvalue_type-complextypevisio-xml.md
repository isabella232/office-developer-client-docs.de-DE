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
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="382ea-102">RowKeyValue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="382ea-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="382ea-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="382ea-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="382ea-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="382ea-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="382ea-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="382ea-105">**Schema file**</span></span> <br/> |<span data-ttu-id="382ea-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="382ea-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="382ea-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="382ea-107">**Extension base**</span></span> <br/> |<span data-ttu-id="382ea-108">Keine</span><span class="sxs-lookup"><span data-stu-id="382ea-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="382ea-109">Definition</span><span class="sxs-lookup"><span data-stu-id="382ea-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="382ea-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="382ea-110">Elements and attributes</span></span>

<span data-ttu-id="382ea-111">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="382ea-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="382ea-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="382ea-112">Child elements</span></span>

<span data-ttu-id="382ea-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="382ea-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="382ea-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="382ea-114">Attributes</span></span>

|<span data-ttu-id="382ea-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="382ea-115">**Attribute**</span></span>|<span data-ttu-id="382ea-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="382ea-116">**Type**</span></span>|<span data-ttu-id="382ea-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="382ea-117">**Required**</span></span>|<span data-ttu-id="382ea-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="382ea-118">**Description**</span></span>|<span data-ttu-id="382ea-119">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="382ea-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="382ea-120">ROWID</span><span class="sxs-lookup"><span data-stu-id="382ea-120">RowID</span></span>  <br/> |<span data-ttu-id="382ea-121">XSD: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="382ea-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="382ea-122">erforderlich</span><span class="sxs-lookup"><span data-stu-id="382ea-122">required</span></span>  <br/> ||<span data-ttu-id="382ea-123">Werte des XSD: unsignedInt-Typs.</span><span class="sxs-lookup"><span data-stu-id="382ea-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="382ea-124">Wert</span><span class="sxs-lookup"><span data-stu-id="382ea-124">Value</span></span>  <br/> |<span data-ttu-id="382ea-125">XSD: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="382ea-125">xsd:string</span></span>  <br/> |<span data-ttu-id="382ea-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="382ea-126">required</span></span>  <br/> ||<span data-ttu-id="382ea-127">Werte des Typs XSD: String.</span><span class="sxs-lookup"><span data-stu-id="382ea-127">Values of the xsd:string type.</span></span>  <br/> |
   

