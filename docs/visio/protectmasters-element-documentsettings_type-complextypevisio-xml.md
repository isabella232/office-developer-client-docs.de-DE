---
title: ProtectMasters-Element (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer Master-Shapes nicht erstellen, bearbeiten oder löschen kann. Der Benutzer kann weiterhin neue Shapes aus einem Master-Shape erstellen, unabhängig von dieser Einstellung.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314819"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="3d5e9-104">ProtectMasters-Element (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3d5e9-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3d5e9-105">Gibt an, ob der Benutzer Master-Shapes nicht erstellen, bearbeiten oder löschen kann.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="3d5e9-106">Der Benutzer kann weiterhin neue Shapes aus einem Master-Shape erstellen, unabhängig von dieser Einstellung.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="3d5e9-107">Der mögliche Wert für dieses Element ist entweder "0" oder "1".</span><span class="sxs-lookup"><span data-stu-id="3d5e9-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="3d5e9-108">Der Wert "0" gibt an, dass Benutzer Master-Shapes erstellen, bearbeiten oder löschen können.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="3d5e9-109">Der Wert "1" gibt an, dass Benutzer keine Master-Shapes erstellen, bearbeiten oder löschen können.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d5e9-110">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3d5e9-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d5e9-111">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-111">**Element type**</span></span> <br/> |[<span data-ttu-id="3d5e9-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="3d5e9-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3d5e9-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3d5e9-114">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-114">**Schema file**</span></span> <br/> |<span data-ttu-id="3d5e9-115">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3d5e9-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3d5e9-116">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-116">**Document parts**</span></span> <br/> |<span data-ttu-id="3d5e9-117">Document. XML</span><span class="sxs-lookup"><span data-stu-id="3d5e9-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3d5e9-118">Definition</span><span class="sxs-lookup"><span data-stu-id="3d5e9-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3d5e9-119">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="3d5e9-119">Elements and attributes</span></span>

<span data-ttu-id="3d5e9-120">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3d5e9-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d5e9-121">Parent elements</span></span>

|<span data-ttu-id="3d5e9-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-122">**Element**</span></span>|<span data-ttu-id="3d5e9-123">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-123">**Type**</span></span>|<span data-ttu-id="3d5e9-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d5e9-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3d5e9-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="3d5e9-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3d5e9-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="3d5e9-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3d5e9-127">Enthält Elemente, die Dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3d5e9-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d5e9-128">Child elements</span></span>

<span data-ttu-id="3d5e9-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d5e9-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d5e9-130">Attributes</span></span>

<span data-ttu-id="3d5e9-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-131">None.</span></span>
  

