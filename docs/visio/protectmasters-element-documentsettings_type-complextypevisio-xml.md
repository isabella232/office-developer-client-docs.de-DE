---
title: ProtectMasters-Element (DocumentSettings_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer erstellen, bearbeiten oder Löschen von master-Shapes verhindert wird. Der Benutzer kann neue Shapes aus einem master-Shape, unabhängig von dieser Einstellung weiterhin erstellen.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797734"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="28b8a-104">ProtectMasters-Element (DocumentSettings_Type ComplexType) ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="28b8a-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="28b8a-105">Gibt an, ob der Benutzer erstellen, bearbeiten oder Löschen von master-Shapes verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="28b8a-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="28b8a-106">Der Benutzer kann neue Shapes aus einem master-Shape, unabhängig von dieser Einstellung weiterhin erstellen.</span><span class="sxs-lookup"><span data-stu-id="28b8a-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="28b8a-107">Der Bereich der möglichen Werte für dieses Element ist "0" oder "1".</span><span class="sxs-lookup"><span data-stu-id="28b8a-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="28b8a-108">Der Wert "0" gibt an, dass Benutzer erstellen, bearbeiten oder Löschen von master-Shapes können.</span><span class="sxs-lookup"><span data-stu-id="28b8a-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="28b8a-109">Der Wert "1" gibt an, dass Benutzer erstellen, bearbeiten oder Löschen von master-Shapes ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="28b8a-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28b8a-110">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28b8a-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28b8a-111">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="28b8a-111">**Element type**</span></span> <br/> |[<span data-ttu-id="28b8a-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="28b8a-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="28b8a-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="28b8a-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="28b8a-114">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="28b8a-114">**Schema file**</span></span> <br/> |<span data-ttu-id="28b8a-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="28b8a-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="28b8a-116">**Dokumentbausteine**</span><span class="sxs-lookup"><span data-stu-id="28b8a-116">**Document parts**</span></span> <br/> |<span data-ttu-id="28b8a-117">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="28b8a-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28b8a-118">Definition</span><span class="sxs-lookup"><span data-stu-id="28b8a-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="28b8a-119">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="28b8a-119">Elements and attributes</span></span>

<span data-ttu-id="28b8a-120">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="28b8a-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="28b8a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28b8a-121">Parent elements</span></span>

|<span data-ttu-id="28b8a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="28b8a-122">**Element**</span></span>|<span data-ttu-id="28b8a-123">**Typ**</span><span class="sxs-lookup"><span data-stu-id="28b8a-123">**Type**</span></span>|<span data-ttu-id="28b8a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28b8a-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="28b8a-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="28b8a-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="28b8a-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="28b8a-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="28b8a-127">Enthält Elemente, die dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="28b8a-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28b8a-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28b8a-128">Child elements</span></span>

<span data-ttu-id="28b8a-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="28b8a-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28b8a-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="28b8a-130">Attributes</span></span>

<span data-ttu-id="28b8a-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="28b8a-131">None.</span></span>
  

