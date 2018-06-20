---
title: HASCATEGORY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797142"
---
# <a name="hascategory-function"></a><span data-ttu-id="7c7ba-103">HASCATEGORY-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c7ba-103">HASCATEGORY Function</span></span>

<span data-ttu-id="7c7ba-104">Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7c7ba-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="7c7ba-105">Version Information</span></span>

<span data-ttu-id="7c7ba-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="7c7ba-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7c7ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c7ba-107">Syntax</span></span>

<span data-ttu-id="7c7ba-108">HASCATEGORY (** *Kategorie* **)</span><span class="sxs-lookup"><span data-stu-id="7c7ba-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7c7ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c7ba-109">Parameters</span></span>

|<span data-ttu-id="7c7ba-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-110">**Name**</span></span>|<span data-ttu-id="7c7ba-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-111">**Required/Optional**</span></span>|<span data-ttu-id="7c7ba-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-112">**Data Type**</span></span>|<span data-ttu-id="7c7ba-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7c7ba-114">_category_</span><span class="sxs-lookup"><span data-stu-id="7c7ba-114">_category_</span></span> <br/> |<span data-ttu-id="7c7ba-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7c7ba-115">Required</span></span>  <br/> |<span data-ttu-id="7c7ba-116">**String**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-116">**String**</span></span> <br/> |<span data-ttu-id="7c7ba-117">Die zu suchende Kategorie.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7c7ba-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c7ba-118">Return value</span></span>

 <span data-ttu-id="7c7ba-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c7ba-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c7ba-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c7ba-120">Remarks</span></span>

 <span data-ttu-id="7c7ba-121">*Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, die Shapes kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="7c7ba-122">Sie können die Kategorien in der Zelle User.msvShapeCategories im ShapeSheet für ein Shape definieren.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="7c7ba-123">Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch ein Semikolon voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

