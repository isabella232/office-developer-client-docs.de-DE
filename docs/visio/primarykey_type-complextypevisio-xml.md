---
title: PrimaryKey_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797731"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="be90c-102">PrimaryKey_Type ComplexType ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="be90c-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="be90c-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="be90c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be90c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be90c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="be90c-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="be90c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="be90c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="be90c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="be90c-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="be90c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="be90c-108">Keine</span><span class="sxs-lookup"><span data-stu-id="be90c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be90c-109">Definition</span><span class="sxs-lookup"><span data-stu-id="be90c-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be90c-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="be90c-110">Elements and attributes</span></span>

<span data-ttu-id="be90c-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="be90c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="be90c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be90c-112">Child elements</span></span>

|<span data-ttu-id="be90c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="be90c-113">**Element**</span></span>|<span data-ttu-id="be90c-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="be90c-114">**Type**</span></span>|<span data-ttu-id="be90c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be90c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be90c-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="be90c-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be90c-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="be90c-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="be90c-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="be90c-118">Attributes</span></span>

|<span data-ttu-id="be90c-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="be90c-119">**Attribute**</span></span>|<span data-ttu-id="be90c-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="be90c-120">**Type**</span></span>|<span data-ttu-id="be90c-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="be90c-121">**Required**</span></span>|<span data-ttu-id="be90c-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be90c-122">**Description**</span></span>|<span data-ttu-id="be90c-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="be90c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="be90c-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="be90c-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="be90c-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="be90c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="be90c-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="be90c-126">required</span></span>  <br/> ||<span data-ttu-id="be90c-127">Werte des Typs xsd: String.</span><span class="sxs-lookup"><span data-stu-id="be90c-127">Values of the xsd:string type.</span></span>  <br/> |
   

