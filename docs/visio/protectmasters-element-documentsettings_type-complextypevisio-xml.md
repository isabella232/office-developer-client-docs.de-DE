---
title: ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Gibt an, ob der Benutzer am Erstellen, Bearbeiten oder Löschen von Masterformen gehindert wird. Der Benutzer kann unabhängig von dieser Einstellung immer noch neue Shapes aus einem Master-Shape erstellen.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540693"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="67d7d-104">ProtectMasters-Element (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="67d7d-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="67d7d-105">Gibt an, ob der Benutzer am Erstellen, Bearbeiten oder Löschen von Masterformen gehindert wird.</span><span class="sxs-lookup"><span data-stu-id="67d7d-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="67d7d-106">Der Benutzer kann unabhängig von dieser Einstellung immer noch neue Shapes aus einem Master-Shape erstellen.</span><span class="sxs-lookup"><span data-stu-id="67d7d-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="67d7d-107">Der Bereich der möglichen Werte für dieses Element ist entweder "0" oder "1".</span><span class="sxs-lookup"><span data-stu-id="67d7d-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="67d7d-108">Der Wert "0" gibt an, dass Benutzer Masterformen erstellen, bearbeiten oder löschen können.</span><span class="sxs-lookup"><span data-stu-id="67d7d-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="67d7d-109">Der Wert "1" gibt an, dass Benutzer Masterformen nicht erstellen, bearbeiten oder löschen können.</span><span class="sxs-lookup"><span data-stu-id="67d7d-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67d7d-110">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="67d7d-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67d7d-111">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="67d7d-111">**Element type**</span></span> <br/> |[<span data-ttu-id="67d7d-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="67d7d-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67d7d-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67d7d-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67d7d-114">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="67d7d-114">**Schema file**</span></span> <br/> |<span data-ttu-id="67d7d-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67d7d-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67d7d-116">**Dokumentteile**</span><span class="sxs-lookup"><span data-stu-id="67d7d-116">**Document parts**</span></span> <br/> |<span data-ttu-id="67d7d-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="67d7d-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67d7d-118">Definition</span><span class="sxs-lookup"><span data-stu-id="67d7d-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67d7d-119">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="67d7d-119">Elements and attributes</span></span>

<span data-ttu-id="67d7d-120">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="67d7d-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67d7d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67d7d-121">Parent elements</span></span>

|<span data-ttu-id="67d7d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="67d7d-122">**Element**</span></span>|<span data-ttu-id="67d7d-123">**Typ**</span><span class="sxs-lookup"><span data-stu-id="67d7d-123">**Type**</span></span>|<span data-ttu-id="67d7d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67d7d-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67d7d-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="67d7d-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67d7d-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="67d7d-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67d7d-127">Enthält Elemente, die Dokumenteinstellungen angeben.</span><span class="sxs-lookup"><span data-stu-id="67d7d-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67d7d-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67d7d-128">Child elements</span></span>

<span data-ttu-id="67d7d-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="67d7d-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67d7d-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="67d7d-130">Attributes</span></span>

<span data-ttu-id="67d7d-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="67d7d-131">None.</span></span>
  

