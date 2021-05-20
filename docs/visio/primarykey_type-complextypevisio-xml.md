---
title: PrimaryKey_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538795"
---
# <a name="primarykey_type-complextype-visio-xml"></a><span data-ttu-id="accba-102">PrimaryKey_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="accba-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="accba-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="accba-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="accba-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="accba-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="accba-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="accba-105">**Schema file**</span></span> <br/> |<span data-ttu-id="accba-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="accba-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="accba-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="accba-107">**Extension base**</span></span> <br/> |<span data-ttu-id="accba-108">Keine</span><span class="sxs-lookup"><span data-stu-id="accba-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="accba-109">Definition</span><span class="sxs-lookup"><span data-stu-id="accba-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="accba-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="accba-110">Elements and attributes</span></span>

<span data-ttu-id="accba-111">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="accba-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="accba-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="accba-112">Child elements</span></span>

|<span data-ttu-id="accba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="accba-113">**Element**</span></span>|<span data-ttu-id="accba-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="accba-114">**Type**</span></span>|<span data-ttu-id="accba-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="accba-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="accba-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="accba-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="accba-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="accba-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="accba-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="accba-118">Attributes</span></span>

|<span data-ttu-id="accba-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="accba-119">**Attribute**</span></span>|<span data-ttu-id="accba-120">**Typ**</span><span class="sxs-lookup"><span data-stu-id="accba-120">**Type**</span></span>|<span data-ttu-id="accba-121">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="accba-121">**Required**</span></span>|<span data-ttu-id="accba-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="accba-122">**Description**</span></span>|<span data-ttu-id="accba-123">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="accba-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="accba-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="accba-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="accba-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="accba-125">xsd:string</span></span>  <br/> |<span data-ttu-id="accba-126">erforderlich</span><span class="sxs-lookup"><span data-stu-id="accba-126">required</span></span>  <br/> ||<span data-ttu-id="accba-127">Werte des xsd:string-Typs.</span><span class="sxs-lookup"><span data-stu-id="accba-127">Values of the xsd:string type.</span></span>  <br/> |
   

